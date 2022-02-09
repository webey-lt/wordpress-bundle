# Migration

## From 1.x to 2.0

In `composer.json` change `"metabolism/wordpress-bundle": "1.4.*"` to `"metabolism/wordpress-bundle": "2.0.*"` then run `composer update -o`

After update

- Remove `src/Service/Context.php`
- Update `src/Controller/BlogController.php`, replace `use App\Service\Context` with `use Metabolism\WordpressBundle\Service\ContextService as Context`
- Update `src/Controller/BlogController.php`, replace `frontAction` with `homeAction`
- Update `public/index.php`, replace `$request` with `$httpRequest`
- Enable `WP Steroids` plugin

Please note that ContextService is deprecated and should be replaced using repository and argurments ( see doc or sample )