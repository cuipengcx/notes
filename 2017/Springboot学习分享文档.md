# **SpringBoot ѧϰ�����ĵ�**
- - - -  - 
## SpringBoot���
- - -
Spring Boot����Pivotal�Ŷ��ṩ��ȫ�¿�ܣ������Ŀ������������SpringӦ�õĳ�ʼ��Լ��������̡��ÿ��ʹ�����ض��ķ�ʽ���������ã��Ӷ�ʹ������Ա������Ҫ�������廯�����á�ͨ�����ַ�ʽ��Spring Boot�����������չ�Ŀ���Ӧ�ÿ�������rapid application development����Ϊ�쵼�ߡ����������spirngboot������http://projects.spring.io/spring-boot/
- - -
## SpringBoot�ص�
- - -

-  ��ѭ��ϰ���������á���ԭ��ʹ��Spring Bootֻ��Ҫ���ٵ����ã��󲿷ֵ�ʱ������ֱ��ʹ��Ĭ�ϵ����ü��ɣ�

-  ��Ŀ���ٴ�������������õ��Զ����ϵ������Ŀ�ܣ�

-  ������ȫ��ʹ��XML�����ļ���ֻ��Ҫ�Զ����ú�Java Config��

-  ��ǶServlet�����������˶Ի�����Ҫ�󣬿���ʹ������ֱ��ִ����Ŀ��Ӧ�ÿ���jar��ִ�У�java -jar��

-  �ṩ��starter POM, �ܹ��ǳ�����Ľ��а�����, �ܴ�̶��ϼ�����jar hell����dependency hell��

-  ������Ӧ��״̬�ļ�أ�

-  ���Ƽ������Ȼ�̳У�

- - -
## SpringBoot�ŵ�
- - -
- SpringBoot�ǰ�����Spring4.0�����ģ�һ���Ƴ��������˾޴�ķ���

- ��������⣬Boot����������˼�����SpringBoot���������߿��ٴSpring��ܣ� 

- SpringBoot���������߿�������һ��Web������ 

- SpringBoot�̳���ԭ��Spring��ܵ��������

- SpringBoot����ʹ��Spring�Ĺ��̣�

- Spring BootΪ���Ǵ����˽ű����Կ�����Ч�ʣ�����Spring Boot��û��������������¼���������Java EE�����߳����Ķ����

## SpringBoot��������� 
- - -
-  Spring Bootʹ������

-  Spring Bootʹ���ñ��

- Spring Bootʹ������

- Spring Bootʹ��ر��

## SpringBoot�ĺ��Ĺ���
- - -
#### ��һ���������е�Spring��Ŀ
  Spring Boot������jar������ʽ���ж��������У�ʹ�ã�java -jar xx.jar �Ϳ��Գɹ���������Ŀ��������Ӧ����Ŀ��������������main�������ɣ�ʹ����Ŀ�Ĳ��𣬵��Զ���ü򵥡�
#### ��������Ƕ��Servlet����
  ��Ƕ������ʹ�����ǿ���ִ��������Ŀ��������main������ʹ��Ŀ�Ŀ������У�
  ���������SpringbootDemoApplication.java
  
  
		import org.springframework.boot.SpringApplication;
		import org.springframework.boot.autoconfigure.SpringBootApplication;

		@SpringBootApplication
		public class SpringbootDemoApplication {

    	public static void main(String[] args) {
        SpringApplication.run(SpringbootDemoApplication.class, args);
   	 		}
		}

#### �������ṩstarter��Manen����
  Spring Boot�ṩ��һϵ�е�starter pom���������ǵ�Maven����,�±��Ǵ���һ����web demo������pom����
		<parent>

			<groupId>org.springframework.boot</groupId>

			<artifactId>spring-boot-starter-parent</artifactId>

			<version>1.5.2.RELEASE</version>

			<relativePath/>

			<!-- lookup parent from repository -->
		</parent>


		<properties>
			<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
			<project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
			<java.version>1.8</java.version>
		</properties>


		<dependencies>
			<dependency>
           		 <groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-starter-web</artifactId>
			</dependency>

			<dependency>
            	<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-starter-test</artifactId>
				<scope>test</scope>
			</dependency>

		</dependencies>


		<build>
		<plugins>
			<plugin>	<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
		</build>
 Spring Boot�������ṩ�˺ܶ��starter pom����ο���
 [http://docs.spring.io/spring-boot/docs/1.5.2.RELEASE/reference/htmlsingle/#boot-documentation](http://docs.spring.io/spring-boot/docs/1.5.2.RELEASE/reference/htmlsingle/#boot-documentation)
 
 
 ���߷���[https://github.com/spring-projects/spring-boot/tree/master/spring-boot-starters](https://github.com/spring-projects/spring-boot/tree/master/spring-boot-starters)
 ͨ�������Ķ�������֪��springboot����Ϊ���������������Ŀ�ܽ�������starter pom���ϣ�������ʹ�õ�ʱ��ֻҪ������ص�
starter��Ȼ��Ϳ���ֱ��ʹ�ã����ߺ��ٵ����ã��Ϳ���ʹ�øÿ�ܵĹ���Ϊ���Ƿ���


#### ���ģ��Զ�����Spring
Spring Boot�����������Ŀ����·����jar��/�࣬Ϊjar����������Զ�����Bean������һ���ʹ��ļ������ǵ����á���Ȼ����ֻ��Spring���ǵ��Ĵ������ʹ�ó�������һЩ������������ǻ���Ҫ�Զ����Զ����ã�

#### ���壩�޴������ɺ�XML����
Spring Boot����ĵط����ǽ����ڴ���������ʵ�ֵģ�����ͨ������ע��ķ�ʽ��ʵ�ֵģ���Ҳ��Spring 4.x�������ԡ�
- - -
##  Spring Boot�Ŀ��ٴ����
- - -
���ǿ���ͨ������[http://start.spring.io/](http://start.spring.io/)�����ٹ���һ��springbootӦ�ã�ѡ��������Ҫ��ģ��󣬻س����ߵ��Generate Project�ͻ�����һ��ѹ��������ѹ������ѹ�������ǵ�ide�Ϳ�������һ��demo��Ŀ������Ҳ����ͨ��idea��SPRING INITIALIZR����������һ��SpringBoot��Ŀ��

## SpringBoot�������̳�̽
- - -
  �Ķ����ǵ�demo���룬���Ƿ�����main����������ִ����һ�������Ĵ���`SpringApplication.run(DemoApplication.class, args);`�鿴run�������������run�����ķ���˵��Ϊ��


		/**
		 * Static helper that can be used to run a {@link 			SpringApplication} from the
	 	* specified source using default settings.
	 	* @param source the source to load
	 	* @param args the application arguments (usually passed from a Java main method)
	 	* @return the running {@link ApplicationContext}
	 	*/
		public static ConfigurableApplicationContext run(Object source, String... args) {
		return run(new Object[] { source }, args);
		}
		
�����˵���ʹ������ǿ��Կ������þ�̬�����������������ǵ�Ӧ�ã����������ʹ��Ĭ�����ã��������������ֱ������ǵ�main�������ڵ��࣬��main�����ķ���������Ȼ������˵�ǰ���µ�����run����������run�������£�


			public static ConfigurableApplicationContext run(Object[] sources, String[] args) {
				return new SpringApplication(sources).run(args);
			}
����η������ǿ������÷���ʵ������һ��SpringApplication,c����Ĳ�����ȻΪӦ����������࣬���ҵ�����SpringApplication�µ�run��String...args)�������������ǲ鿴ʵ�����ķ�����Ҳ����SpringApplication�Ĺ��캯���� 
 

			public SpringApplication(Object... sources) {
				initialize(sources);
			}

�鿴initialize������


	@SuppressWarnings({ "unchecked", "rawtypes" })
	private void initialize(Object[] sources) {
		if (sources != null && sources.length > 0) {
			this.sources.addAll(Arrays.asList(sources));
		}
		this.webEnvironment = deduceWebEnvironment();
		setInitializers((Collection) getSpringFactoriesInstances(
				ApplicationContextInitializer.class));
		setListeners((Collection) getSpringFactoriesInstances(ApplicationListener.class));
		this.mainApplicationClass = deduceMainApplicationClass();
	}
����Ĵ�����Կ�����ʼ�������������¼������� 
this.webEnvironment = deduceWebEnvironment(); 
��һ������������������һ��WEBӦ�û���һ��SPRING�ı�׼StandaloneӦ�á����������Կ���������ô�жϵģ� 


		private boolean deduceWebEnvironment() {
			for (String className : WEB_ENVIRONMENT_CLASSES) {
				if (!ClassUtils.isPresent(className, null)) {
				return false;
			}
		}
		return true;
	}

���Կ����Ǹ���org.springframework.util.ClassUtils�ľ�̬����ȥ�ж�classpath�����Ƿ���WEB_ENVIRONMENT_CLASSES�������࣬����ж������򷵻�true���ʾ����һ��WEBӦ�ã����򷵻�false����һ����׼Spring��Ӧ�á�Ȼ��ͨ�����룺

	private static final String[] WEB_ENVIRONMENT_CLASSES = 
          { "javax.servlet.Servlet",
            "org.springframework.web.context.ConfigurableWebApplicationContext" };

���Կ����Ƿ�����һ��WEBӦ�þ���ȡ����classpath���Ƿ���javax.servlet.Servlet�� 
org.springframework.web.context.ConfigurableWebApplicationContext��Ȼ�������һ���׶Σ�		


	setInitializers((Collection) getSpringFactoriesInstances(ApplicationContextInitializer.class));
    
��������ǳ�ʼ��classpath�µ����еĿ��õ�ApplicationContextInitializer

	setListeners((Collection) getSpringFactoriesInstances(ApplicationListener.class));
    
��������ǳ�ʹ��classpath�µ����еĿ��õ�ApplicationListener��
����ִ��deduceMainApplicationClass�������ҳ�main������ȫ������������ʵ�������õ�SpringApplication��this.mainApplicationClass��ɳ�ʼ����

		private Class<?> deduceMainApplicationClass() {
		try {
			StackTraceElement[] stackTrace = new RuntimeException().getStackTrace();
			for (StackTraceElement stackTraceElement : stackTrace) {
				if ("main".equals(stackTraceElement.getMethodName())) {
					return Class.forName(stackTraceElement.getClassName());
				}
			}
		}
		catch (ClassNotFoundException ex) {
			// Swallow and continue
		}
		return null;
	}
    
Ȼ�����SpringApplicationʵ����run����������Ӧ�ã��������£�


		/**
	 * Run the Spring application, creating and refreshing a new
	 * {@link ApplicationContext}.
	 * @param args the application arguments (usually passed from a Java main method)
	 * @return a running {@link ApplicationContext}
	 */
	public ConfigurableApplicationContext run(String... args) {
		StopWatch stopWatch = new StopWatch();
		stopWatch.start();
		ConfigurableApplicationContext context = null;
		FailureAnalyzers analyzers = null;
		configureHeadlessProperty();
		SpringApplicationRunListeners listeners = getRunListeners(args);
		listeners.starting();
		try {
			ApplicationArguments applicationArguments = new DefaultApplicationArguments(
					args);
			ConfigurableEnvironment environment = prepareEnvironment(listeners,
					applicationArguments);
			Banner printedBanner = printBanner(environment);
			context = createApplicationContext();
			analyzers = new FailureAnalyzers(context);
			prepareContext(context, environment, listeners, applicationArguments,
					printedBanner);
			refreshContext(context);
			afterRefresh(context, applicationArguments);
			listeners.finished(context, null);
			stopWatch.stop();
			if (this.logStartupInfo) {
				new StartupInfoLogger(this.mainApplicationClass)
						.logStarted(getApplicationLog(), stopWatch);
			}
			return context;
		}
		catch (Throwable ex) {
			handleRunFailure(context, listeners, analyzers, ex);
			throw new IllegalStateException(ex);
		}
	}

���ǿ��Կ�������δ�����Ϊ����Ӧ�������ľ���ʵ�֣����ǱȽϸ��ӵģ�Ŀǰ��֪��������SpringApplicationRunListener�����������ĳ�ʼ�����̽��м�����


		SpringApplicationRunListeners listeners = getRunListeners(args);
		listeners.starting();
		
Ȼ�����ǲ鿴���漸�д��룺


	ApplicationArguments applicationArguments = new DefaultApplicationArguments(args);
	ConfigurableEnvironment environment = prepareEnvironment(listeners, applicationArguments);
	Banner printedBanner = printBanner(environment);
	context = createApplicationContext();
	prepareContext(context, environment, listeners, applicationArguments, printedBanner);
	refreshContext(context);
	afterRefresh(context, applicationArguments);


�����ǻ�ȡ����ʱ�������args����ʼ��ΪApplicationArguments���� 
SpringApplication.run(Application.class, args);ȡ���ﴫ��ֵ�� 
Ȼ������SpringBootӦ�õĻ�����


	ConfigurableEnvironment environment = prepareEnvironment(listeners, applicationArguments);

Ȼ�����������ǱȽϺ��ĵģ�
	
    context = createApplicationContext();
	prepareContext(context, environment, listeners, applicationArguments, printedBanner);
	refreshContext(context);
	afterRefresh(context, applicationArguments);
    
������createApplicationContext()������
	
    protected ConfigurableApplicationContext createApplicationContext() {
    Class<?> contextClass = this.applicationContextClass;
    if (contextClass == null) {
        try {
            contextClass = Class.forName(this.webEnvironment
                    ? DEFAULT_WEB_CONTEXT_CLASS : DEFAULT_CONTEXT_CLASS);
        }
        catch (ClassNotFoundException ex) {
            throw new IllegalStateException(
                    "Unable create a default ApplicationContext, "
                            + "please specify an ApplicationContextClass",
                    ex);
        }
    }
    return (ConfigurableApplicationContext) BeanUtils.instantiate(contextClass);
	}

���Կ���������ǰ��ʼ�����̳�ʼ����this.webEnvironment��������ʼ��һ��ʲô���������classpath���Ƿ���javax.servlet.Servlet�� 
org.springframework.web.context.ConfigurableWebApplicationContext�࣬ 
��ʹ��DEFAULT_WEB_CONTEXT_CLASS��ʼ���������������������DEFAULT_CONTEXT_CLASS��ʼ��������
��������Ĵ���������Ȼ��ִ�����µļ�������������������Ĵ����������Լ�bean��ע�빦�ܡ�

	prepareContext(context, environment, listeners, applicationArguments, printedBanner);
    
������һ�������ʵ��spring-boot-starter-*���Զ������õĹؼ���


	refreshContext(context);
	afterRefresh(context, applicationArguments);
	
����refreshContext�����ApplicationContext�������������
prepareBeanFactory������postProcessBeanFactory������������ע�ᣬ��Ϣ����ʼ���ȵȲ�����������Բ鿴AbstractApplicationContext���µ�refresh()������
afterRefresh����ʵ����ʹ�õ���callRunners(context, args);�������������£�

		private void callRunners(ApplicationContext context, ApplicationArguments args) {
		List<Object> runners = new ArrayList<Object>();
		runners.addAll(context.getBeansOfType(ApplicationRunner.class).values());
		runners.addAll(context.getBeansOfType(CommandLineRunner.class).values());
		AnnotationAwareOrderComparator.sort(runners);
		for (Object runner : new LinkedHashSet<Object>(runners)) {
			if (runner instanceof ApplicationRunner) {
				callRunner((ApplicationRunner) runner, args);
			}
			if (runner instanceof CommandLineRunner) {
				callRunner((CommandLineRunner) runner, args);
			}
		}
	}

���Կ��������������е�bean����һ��ListȻ��ѭ��ע�ᣬ����ֵ��ע���callRunner����������ApplicationRunner�ӿڵ�run����������ִ��bean��
 ������Ϊֹ�������������������̻�����ɣ����еĸ���Listener������Environment��Environment�ĳ�ʼ�������ݶ�û������������Ľ�������ʱ�������Ȥ���Լ����鿴Դ����

## SpringBoot�Զ����ý���
- - - 

�����ȿ�@SpringBootApplicationע�⣺

	@Target(ElementType.TYPE)
	@Retention(RetentionPolicy.RUNTIME)
	@Documented
	@Inherited
	@SpringBootConfiguration
	@EnableAutoConfiguration
	@ComponentScan(excludeFilters = {
		@Filter(type = FilterType.CUSTOM, classes = TypeExcludeFilter.class),
		@Filter(type = FilterType.CUSTOM, classes = AutoConfigurationExcludeFilter.class) })
 
��������@Target��@Retention��@Documented��@Inherited���ĸ�ע��ΪԪע��������@ComponentScan�����Spring�ܳ��õ�ע�⣬Ҳ�����������ȿ�@SpringBootConfiguration��


	@Target(ElementType.TYPE)
	@Retention(RetentionPolicy.RUNTIME)
	@Documented
	@Configuration
	public @interface SpringBootConfiguration {

	}
���ע�������@Configuration��ע��ǰ��Ϊ��JavaConfig�� ��Ȼ����������@EnableAutoConfigurationע��

	@SuppressWarnings("deprecation")
	@Target(ElementType.TYPE)
	@Retention(RetentionPolicy.RUNTIME)
	@Documented
	@Inherited
	@AutoConfigurationPackage
	@Import(EnableAutoConfigurationImportSelector.class)

���ע����@Import(EnableAutoConfigurationImportSelector.class)��������������Spring��JavaConfig���Ž���EnableAutoConfigurationImportSelector.class 
���Ƿ��ָ���̳���AutoConfigurationImportSelector��Ȼ�����ǲ鿴������ķ�����
	
		@Override
	public String[] selectImports(AnnotationMetadata annotationMetadata) {
		if (!isEnabled(annotationMetadata)) {
			return NO_IMPORTS;
		}
		try {
			AutoConfigurationMetadata autoConfigurationMetadata = AutoConfigurationMetadataLoader
					.loadMetadata(this.beanClassLoader);
			AnnotationAttributes attributes = getAttributes(annotationMetadata);
			List<String> configurations = getCandidateConfigurations(annotationMetadata,
					attributes);
			configurations = removeDuplicates(configurations);
			configurations = sort(configurations, autoConfigurationMetadata);
						Set<String> exclusions = getExclusions(annotationMetadata, attributes);
			checkExcludedClasses(configurations, exclusions);
			configurations.removeAll(exclusions);
			configurations = filter(configurations, autoConfigurationMetadata);
			fireAutoConfigurationImportEvents(configurations, exclusions);
			return configurations.toArray(new String[configurations.size()]);
		}
		catch (IOException ex) {
			throw new IllegalStateException(ex);
		}
	}

���룺List configurations = getCandidateConfigurations(metadata,attributes);


		protected List<String> getCandidateConfigurations(AnnotationMetadata metadata,
			AnnotationAttributes attributes) {
		List<String> configurations = SpringFactoriesLoader.loadFactoryNames(
				getSpringFactoriesLoaderFactoryClass(), getBeanClassLoader());
		Assert.notEmpty(configurations,
				"No auto configuration classes found in META-INF/spring.factories. If you "
						+ "are using a custom packaging, make sure that file is correct.");
		return configurations;
	}
    
�ڽ��룺List configurations = SpringFactoriesLoader.loadFactoryNames( 
getSpringFactoriesLoaderFactoryClass(), getBeanClassLoader()); ��������:



		public static List<String> loadFactoryNames(Class<?> factoryClass, ClassLoader classLoader) {
		String factoryClassName = factoryClass.getName();
		try {
			Enumeration<URL> urls = (classLoader != null ? classLoader.getResources(FACTORIES_RESOURCE_LOCATION) :
					ClassLoader.getSystemResources(FACTORIES_RESOURCE_LOCATION));
			List<String> result = new ArrayList<String>();
			while (urls.hasMoreElements()) {
				URL url = urls.nextElement();
				Properties properties = PropertiesLoaderUtils.loadProperties(new UrlResource(url));
				String factoryClassNames = properties.getProperty(factoryClassName);
				result.addAll(Arrays.asList(StringUtils.commaDelimitedListToStringArray(factoryClassNames)));
			}
			return result;
		}
				catch (IOException ex) {
			throw new IllegalArgumentException("Unable to load [" + factoryClass.getName() +
					"] factories from location [" + FACTORIES_RESOURCE_LOCATION + "]", ex);
		}
	}
	
������Ĵ�����Կ����Զ�������������ݴ����factoryClass.getName()��spring.factories���ļ����ҵ���Ӧ��key���Ӷ�����������࣬������ô���صĲο� **SpringBoot�������̳�̽**������refreshContext(context);ʵ�֡����ǿ���ͨ���鿴spring-boot-autoconfigure-1.5.2.RELEASE.jar�µ�META-INF���spring.factories�鿴SpringBoot��֧�ֵ��Զ����õ���/��������ܡ�������org.springframework.boot.autoconfigure.data.Redis.RedisAutoConfigurationΪ���鿴�������£�

	@Configuration
	@ConditionalOnClass({ JedisConnection.class, RedisOperations.class, Jedis.class })
	@EnableConfigurationProperties(RedisProperties.class)
	public class RedisAutoConfiguration {
    @Configuration
    @ConditionalOnClass(GenericObjectPool.class)
    protected static class RedisConnectionConfiguration {
        @Bean
        @ConditionalOnMissingBean(RedisConnectionFactory.class)
        public JedisConnectionFactory redisConnectionFactory()
                throws UnknownHostException {
            return applyProperties(createJedisConnectionFactory());
        }
    }
	   @Configuration
    protected static class RedisConfiguration {
        @Bean
        @ConditionalOnMissingBean(name = "redisTemplate")
        public RedisTemplate<Object, Object> redisTemplate(
                RedisConnectionFactory redisConnectionFactory)
                        throws UnknownHostException {
            RedisTemplate<Object, Object> template = new RedisTemplate<Object, Object>();
            template.setConnectionFactory(redisConnectionFactory);
            return template;
        }
        @Bean
        @ConditionalOnMissingBean(StringRedisTemplate.class)
        public StringRedisTemplate stringRedisTemplate(
                RedisConnectionFactory redisConnectionFactory)
                        throws UnknownHostException {
            StringRedisTemplate template = new StringRedisTemplate();
            template.setConnectionFactory(redisConnectionFactory);
            return template;
        }

    }
	��
	
 �����һ�»����ϾͿ��Կ��������һ��Spring��ע�������� 
@ConditionalOnClass({ JedisConnection.class, RedisOperations.class, Jedis.class })���ע�����˼�ǣ�������JedisConnection.class, RedisOperations.class, Jedis.class������ʱ�Ž���RedisAutoConfiguration������,���򲻽�����һ�������� 
@ConditionalOnMissingBean(name = ��redisTemplate��)���ע�����˼����������в�����nameָ����bean�򴴽�beanע�룬����ִ�� 
�ڲ�������Կ��������ֶ�����������@Configurationע��������࣬���������������SpringIOC����ע�����3��bean�� 
���ȵ���·���´���(GenericObjectPool.class)ʱ��ע��JedisConnectionFactory ��ʵ�����Spring�����в�����name = ��redisTemplate����ʵ�壬�򴴽�RedisTemplate��StringRedisTemplateʵ��ע��������������Spring����Ŀ�У��Ϳ������������Spring�����bean��ע����RedisTemplate��StringRedisTemplate��ʵ������redis��������ˡ� 
ͨ�����Ϸ����Ĺ������ǿ��Է���ֻҪһ������SpringBoot��Ŀ����·���´���JedisConnection.class, RedisOperations.class, Jedis.class�Ϳ��Դ����Զ�������,��˼˵����ֻҪ��maven����Ŀ��������spring-data-redis-1.7.2.RELEASE.jar��C:jedis-2.8.2.jar�Ϳ��Դ����Զ�����,����������ÿ����һ�����ܶ�Ҫȥ���������Զ��������࣬�Ǿʹ��������伴�õ�Ч���ˡ�����Spring-bootΪ���ṩ��ͳһ��starter����ֱ�����ú���ش����Զ����õ����е������������redis��start���£�

    <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-redis</artifactId>
	</dependency>
    

 
 Ȼ�����ǵ��artifactId���Է��֣�spring-boot-starter-data-redis��Դ����pom.xml�ļ�����������:
  
 	<dependencies>
    	<dependency>
        	<groupId>org.springframework.boot</groupId>
        	<artifactId>spring-boot-starter</artifactId>
    	</dependency>
    	<dependency>
        	<groupId>org.springframework.data</groupId>
        	<artifactId>spring-data-redis</artifactId>
    	</dependency>
    	<dependency>
        	<groupId>redis.clients</groupId>
        	<artifactId>jedis</artifactId>
    	</dependency>
	</dependencies>
    
��Ϊmaven�����Ĵ����ԣ�����ֻҪ����starter�Ϳ��Կ�����·�������ú����еĴ����Զ����õ������࣬ʵ�ֿ��伴�õĹ��ܡ�ͨ�������springboot�Զ�����ԭ�����⣬�������������Լ������Լ�ר�е�starterҲ���Ǻ����ѵģ�ֻ��Ҫ��չһ��spring.factories��Ȼ��������һ���Լ�ӵ�е�config�����������Ҫ�����Ĺ���Ϳ����ˡ�



























		

		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		