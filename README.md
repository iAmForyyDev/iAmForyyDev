```java
public class iAmForyyDev extends GitHubUser {

  public iAmForyyDev(){
    super("iAmForyyDev_", "Perú", 18);
    
    this.addLanguage(Language.JAVA); 
    this.addLearningLanguage(
      Language.HTML
      Language.CSS,
      Language.JAVASCRIPT
    );
    
    this.addExperience(
      "Spigot API", 
      "Configurator", 
      "Setups Creator",
      "Furious Studios",
      "Furious Community"
    );
  }
}

public abstract class GitHubUser {

  @Getter private final String username;
  @Getter private final String country;
  @Getter private final int age;

  private final Set<String> experiences = new HashSet<>();
  private final Set<Language> languages = new HashSet<>();
  private final Set<Language> learningLanguage = new HashSet<>(); // General Languages

  public GitHubUser(
      String username, 
      String country, 
      int age
      
  ) {
  
      this.name = username;
      this.country = country;
      this.age = age;
  }

  public void addLanguage(
      Language... language
  ) {
      this.languages.addAll(language);
  }
  
  public void addExperience(
      String... experience
  ) {
      this.experiences.addAll(experience);
  }
  
  public void addLearningLanguage(
      Language... languages
  ){
      this.learningLanguage.addAll(languages);
  } 
}

public enum Language {

  HTML,
  CSS,
  
  JAVA,
  JAVASCRIPT,
  TYPESCRIPT,
  PYTHON,
  PHP,
  C#,
  C++

}
```
