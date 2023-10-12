```php
<?php
class Tomsjac
{
    public function __construct(
        private string $fullName = "Thomas Jacquey",
        private array $roles = ['Chef de projet', 'Lead Développeur', 'Développeur'],
        private array $skills = ['PHP', 'Laravel', 'Docker', 'Gitlab', 'Sql', 'VueJs'],
    ) {}

    public function display(): string
    {
        $greetingMessage = <<<HELLO
            Bonjour! 
            Je m'appelle {$this->fullName}.
	        Je suis un {$this->roles[array_rand($this->roles)]}
            HELLO;

        return  $greetingMessage . PHP_EOL;
    }

    public function experience(): array
    {
        return [
            [
                'dates' => ['start' => '2009-01-01' , 'end' => null],
                'company' => 'Plus que PRO',
                'job' => 'Lead développeur'
            ],
            [
                'dates' => ['start' => '2010-01-01' , 'end' => '2019-01-01'],
                'company' => 'WebCD',
                'job' => 'Chef de projet technique'
            ],
            [
                'dates' => ['start' => '2006-07-01' , 'end' => '2009-12-31'],
                'company' => 'WebCD',
                'job' => 'Développeur PHP extranet'
            ],
            [
                'dates' => ['start' => '2003-09-01' , 'end' => '2006-05-31'],
                'company' => 'E-Maginair',
                'job' => 'Développeur Web'
            ],
        ];

    }

    public function links(): array
    {
        return [
            'portfolio' => 'https://wwww.tomsjac.info',
            'twitter' => '@tomsjac',
            'linkedin' => 'https://fr.linkedin.com/in/tomsjac'
        ];
        
    }
}
```