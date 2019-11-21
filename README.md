# SwaggerConsulta



XXXXXXXXXXXXXXxXXpom

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>teste.com</groupId>
  <artifactId>main</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>jar</packaging>

  <name>teste-ec</name>
  <description>Teste ECO</description>


	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.0.4.RELEASE</version>
		<relativePath /> <!-- lookup parent from repository -->
	</parent>

	<properties>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
		<java.version>1.8</java.version>
		<swagger.version>2.9.2</swagger.version>
	</properties>

	<dependencies>
		<dependency>
			<groupId>org.apache.cxf</groupId>
			<artifactId>cxf-spring-boot-starter-jaxws</artifactId>
			<version>3.3.1</version>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-validation</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>

		<dependency>
			<groupId>org.junit.jupiter</groupId>
			<artifactId>junit-jupiter-engine</artifactId>
			<scope>test</scope>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-actuator</artifactId>
		</dependency>

		<dependency>
			<groupId>io.springfox</groupId>
			<artifactId>springfox-swagger2</artifactId>
			<version>${swagger.version}</version>
			<!-- Exclusão efetuada como sugestão para o bug: https://github.com/swagger-api/swagger-core/issues/2979#issuecomment-433273332 -->
			<exclusions>
				<exclusion>
					<groupId>io.swagger</groupId>
					<artifactId>swagger-models</artifactId>
				</exclusion>
			</exclusions>
		</dependency>
		<!-- Importando separadamente como sugestão para o bug: https://github.com/swagger-api/swagger-core/issues/2979#issuecomment-433273332 -->
		<dependency>
			<groupId>io.swagger</groupId>
			<artifactId>swagger-models</artifactId>
			<version>1.5.21</version>
		</dependency>

		<dependency>
			<groupId>io.springfox</groupId>
			<artifactId>springfox-swagger-ui</artifactId>
			<version>${swagger.version}</version>
		</dependency>

		<dependency>
			<groupId>io.swagger.core.v3</groupId>
			<artifactId>swagger-annotations</artifactId>
			<version>2.0.8</version>
		</dependency>

		<dependency>
			<groupId>org.apache.httpcomponents</groupId>
			<artifactId>httpcore</artifactId>
		</dependency>

		<dependency>
			<groupId>org.apache.httpcomponents</groupId>
			<artifactId>httpclient</artifactId>
		</dependency>

		<dependency>
			<groupId>org.apache.commons</groupId>
			<artifactId>commons-lang3</artifactId>
		</dependency>

		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-jdbc</artifactId>
		</dependency>
		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
		</dependency>

		<dependency>
			<groupId>com.oracle</groupId>
			<artifactId>ojdbc7</artifactId>
			<version>12.1.0.2</version>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-configuration-processor</artifactId>
		</dependency>

		<dependency>
			<groupId>ch.qos.logback</groupId>
			<artifactId>logback-classic</artifactId>
		</dependency>

		<dependency>
			<groupId>ch.qos.logback.contrib</groupId>
			<artifactId>logback-json-classic</artifactId>
			<version>0.1.5</version>
		</dependency>

		<dependency>
			<groupId>ch.qos.logback.contrib</groupId>
			<artifactId>logback-jackson</artifactId>
			<version>0.1.5</version>
		</dependency>

		<dependency>
			<groupId>com.fasterxml.jackson.core</groupId>
			<artifactId>jackson-databind</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-activemq</artifactId>
		</dependency>

		<dependency>
		    <groupId>com.google.code.gson</groupId>
		    <artifactId>gson</artifactId>
		    <version>2.8.5</version>
		</dependency>

        <dependency>
            <groupId>org.modelmapper</groupId>
            <artifactId>modelmapper</artifactId>
            <version>2.3.0</version>
        </dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<configuration>
					<source>${java.version}</source>
					<target>${java.version}</target>
				</configuration>
			</plugin>
		</plugins>
	</build>
</project>



xxxxxxxxxxxxxxxxxTesteEc

package teste.com;


import java.util.concurrent.Executor;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.AutoConfigurationPackage;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.annotation.Bean;
import org.springframework.scheduling.annotation.EnableAsync;
import org.springframework.scheduling.concurrent.ThreadPoolTaskExecutor;
import javax.swing.JOptionPane;


@EnableAsync
@AutoConfigurationPackage
@SpringBootApplication

public class App 
{
    public static void main( String[] args )
    {
        System.setProperty("server.servlet.conext-path","/teste-ec");
        SpringApplication.run(App.class, args);
        
        System.out.println("Serviço Iniciado");
        JOptionPane.showMessageDialog(null,"Serviço Iniciado");
        
        
    }
    @Bean
    public Executor taskExecutor() {
    	ThreadPoolTaskExecutor executor = new ThreadPoolTaskExecutor();
    	executor.setCorePoolSize(2);
    	executor.setMaxPoolSize(2);
    	executor.setQueueCapacity(500);
    	executor.setThreadNamePrefix("Assincrono");
    	executor.initialize();
    	return executor;
    }
 
    }

xxxxxxxxxxxxxxxxxxTesteEC2

package teste.com.api;
  
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import io.swagger.annotations.Api;

@CrossOrigin
@RestController
@RequestMapping(value = "/")
@Api(value = "/", description = "Teste")

public class TesteEC2 {


	
	@GetMapping(value = "consulta-EC2A")
	public String criacao() {
		String teste = "Validado Teste";
		return teste;
	}
	 @GetMapping(value = "consulta-EC2B")
		public String criacao2() {
			String teste2 = "Validado Teste 2";
			return teste2;
	}
 
@GetMapping(value = "consulta-EC2C")
	public String criacao3() {
		String teste3 = "Validado Teste 3";
		return teste3;
}




}

XXXXXXXXXXXXXXXXXXXApp
package teste.com;


import java.util.concurrent.Executor;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.AutoConfigurationPackage;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.annotation.Bean;
import org.springframework.scheduling.annotation.EnableAsync;
import org.springframework.scheduling.concurrent.ThreadPoolTaskExecutor;
import javax.swing.JOptionPane;


@EnableAsync
@AutoConfigurationPackage
@SpringBootApplication

public class App 
{
    public static void main( String[] args )
    {
        System.setProperty("server.servlet.conext-path","/teste-ec");
        SpringApplication.run(App.class, args);
        
        System.out.println("Serviço Iniciado");
        JOptionPane.showMessageDialog(null,"Serviço Iniciado");
        
        
    }
    @Bean
    public Executor taskExecutor() {
    	ThreadPoolTaskExecutor executor = new ThreadPoolTaskExecutor();
    	executor.setCorePoolSize(2);
    	executor.setMaxPoolSize(2);
    	executor.setQueueCapacity(500);
    	executor.setThreadNamePrefix("Assincrono");
    	executor.initialize();
    	return executor;
    }
 
    }

xxxxxxxxxxxxWebConfig

package teste.com.config;

import java.security.KeyManagementException;
import java.security.KeyStoreException;
import java.security.NoSuchAlgorithmException;
import java.security.cert.X509Certificate;

import javax.net.ssl.SSLContext;

import org.apache.http.conn.ssl.SSLConnectionSocketFactory;
import org.apache.http.impl.client.CloseableHttpClient;
import org.apache.http.impl.client.HttpClients;
import org.apache.http.ssl.TrustStrategy;
import org.springframework.context.MessageSource;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.context.support.ReloadableResourceBundleMessageSource;
import org.springframework.http.client.HttpComponentsClientHttpRequestFactory;
import org.springframework.validation.Validator;
import org.springframework.validation.beanvalidation.LocalValidatorFactoryBean;
import org.springframework.web.client.RestTemplate;
import org.springframework.web.servlet.config.annotation.CorsRegistry;
import org.springframework.web.servlet.config.annotation.EnableWebMvc;
import org.springframework.web.servlet.config.annotation.ResourceHandlerRegistry;
import org.springframework.web.servlet.config.annotation.ViewControllerRegistry;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;

@Configuration
@EnableWebMvc
public class WebConfig implements WebMvcConfigurer {

	@Bean
	public RestTemplate restTemplate() throws KeyManagementException, NoSuchAlgorithmException, KeyStoreException {
		TrustStrategy acceptingTrustStrategy = (X509Certificate[] chain, String authType) -> true;

		SSLContext sslContext = org.apache.http.ssl.SSLContexts.custom().loadTrustMaterial(null, acceptingTrustStrategy).build();

		SSLConnectionSocketFactory csf = new SSLConnectionSocketFactory(sslContext);

		CloseableHttpClient httpClient = HttpClients.custom().setSSLSocketFactory(csf).build();

		HttpComponentsClientHttpRequestFactory requestFactory = new HttpComponentsClientHttpRequestFactory();

		requestFactory.setHttpClient(httpClient);
		RestTemplate restTemplate = new RestTemplate(requestFactory);
		return restTemplate;
	}

	@Override
	public void addViewControllers(ViewControllerRegistry registry) {
		registry.addRedirectViewController("/v2/api-docs", "/v2/api-docs");
		registry.addRedirectViewController("/swagger-resources/configuration/ui", "/swagger-resources/configuration/ui");
		registry.addRedirectViewController("/swagger-resources/configuration/security",
				"/swagger-resources/configuration/security");
		registry.addRedirectViewController("/swagger-resources", "/swagger-resources");
	}

	@Override
	public void addResourceHandlers(ResourceHandlerRegistry registry) {
		registry.addResourceHandler("/swagger-ui.html**").addResourceLocations("classpath:/META-INF/resources/swagger-ui.html");
		registry.addResourceHandler("/webjars/**").addResourceLocations("classpath:/META-INF/resources/webjars/");
	}

	@Override
	public void addCorsMappings(CorsRegistry registry) {
		registry.addMapping("/**").allowedOrigins("*");
	}

	@Bean
	public MessageSource messageSource() {
		ReloadableResourceBundleMessageSource messageSource = new ReloadableResourceBundleMessageSource();
		messageSource.setBasename("classpath:messages");
		messageSource.setDefaultEncoding("UTF-8");
		return messageSource;
	}

	@Bean
	@Override
	public Validator getValidator() {
		LocalValidatorFactoryBean bean = new LocalValidatorFactoryBean();
		bean.setValidationMessageSource(messageSource());
		return bean;
	}
}
