```java
public final class iAmForyyDev extends GitHubUser {

  public iAmForyyDev() {
    super("iAmForyyDev_", "Peru", 20);

    // "Yep, I Love java"
    this.addLanguage(
      Language.JAVA,
      Language.PYTHON
    );
 
    this.addLearningLanguage(
      Language.JAVASCRIPT,
      Language.TYPESCRIPT
    );
    
    this.addExperience(
      "Spigot API",
      "Paper API",
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

  public GitHubUser(String username, String country, int age) {
      this.name = username;
      this.country = country;
      this.age = age;
  }

  public void addLanguage(Language... language) {
      this.languages.addAll(language);
  }
  
  public void addExperience(String... experience) {
      this.experiences.addAll(experience);
  }
  
  public void addLearningLanguage(Language... languages){
      this.learningLanguage.addAll(languages);
  } 
}

public enum Language {

  HTML,
  CSS,
  
  JAVA,
  KOTLIN,
  JAVASCRIPT,
  TYPESCRIPT,
  PYTHON,
  PHP,
  RUBIK,
  GO

}
```
<img src="github_snake.svg" alt="Descripción">
