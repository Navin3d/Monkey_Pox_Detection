# Monkey_Pox_Detection
This is an Project used to find whether person suffering from Monkey Pox or not.

## Setup Mac-OS:

 - https://medium.com/@jarondlk/installing-tensorflow-metal-on-apple-silicon-macos-with-miniconda-f43121fe3054
 - https://medium.com/@yningz/how-to-install-and-actually-run-with-tensorflow-on-m1-m2-mac-with-metal-plugin-in-3-steps-81341d0a9363
 - https://forums.developer.apple.com/forums/thread/768858
 - https://forums.developer.apple.com/forums/tags/tensorflow-metal

```
import javax.sql.DataSource;
import org.springframework.jdbc.datasource.DriverManagerDataSource;

@Configuration
public class DataSourceConfig {

    @Value("${spring.datasource.url}")
    private String url;

    @Value("${spring.datasource.username}")
    private String username;

    @Value("${spring.datasource.password}")
    private String encodedPassword;

    @Bean
    public DataSource dataSource() {
        DriverManagerDataSource dataSource = new DriverManagerDataSource();
        dataSource.setUrl(url);
        dataSource.setUsername(username);
        dataSource.setPassword(PasswordDecoder.decode(encodedPassword));
        return dataSource;
    }
}
```

```bash
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh

conda create --name venv python=3.9

conda activate tf

conda install -c apple tensorflow-deps --force-reinstall -n tf

conda install cudatoolkit=9.0 tensorflow-gpu=1.11.0

python3 -m pip install tensorflow-macos==2.9

python3 -m pip install tensorflow-metal==0.5.0    // dont use this

python3 -m pip list | grep tensorflow

python3 -m pip install scipy

conda deactivate
```

```
active ones are venv, tf, tf-env, torch

conda activate tf-env

jupyter lab
```
