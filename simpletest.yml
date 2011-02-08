--- 
simpletest: |-
  <?php
    /**
     * A unit test class with all available functions
     */
    require 'simpletest/autorun.php';
    class HelloTest extends UnitTestCase {
  
      function setUp() {
        // Runs this before each test method
      }
  
      function tearDown() {
        // Runs this after each test method
      }
  
      function testHello() {
        // Fail if $x is false
        $x = true;
        $this->assertTrue($x);
  
        // Fail if $x is true
        $this->assertFalse($x);
  
        // Fail if $x is set
        $this->assertNull($x);
  
        // Fail if $x not set
        $this->assertNotNull($x);
  
        // Fail if $x is not the class or type $t
        $this->assertIsA($x, $t);
  
        // Fail if $x is of the class or type $t
        $this->assertNotA($x, $t);
  
        // Fail if $x == $y is false
        $this->assertEqual($x, $y);
  
        // Fail if $x == $y is true
        $this->assertNotEqual($x, $y);
  
        // Fail if abs($x - $y) < $m is false
        $this->assertWithinMargin($x, $y, $m);
  
        // Fail if abs($x - $y) < $m is true
        $this->assertOutsideMargin($x, $y, $m);
  
        // Fail if $x == $y is false or a type mismatch
        $this->assertIdentical($x, $y);
  
        // Fail if $x == $y is true and types match
        $this->assertNotIdentical($x, $y);
  
        // Fail unless $x and $y are the same variable
        $this->assertReference($x, $y);
  
        // Fail unless $x and $y are identical copies
        $this->assertClone($x, $y);
  
        // Fail unless the regex $p matches $x
        $this->assertPattern($p, $x);
  
        // Fail if the regex $p matches $x
        $this->assertNoPattern($p, $x);
  
        // Swallows any upcoming matching error
        $this->expectError($x);
  
        // Fail on failed expectation object $e
        $this->assert($e);
  
        // Sends a test pass
        $this->pass();
  
        // Sends a test failure
        $this->fail();
  
        // Sends an exception event
        $this->error();
  
        // Sends a user defined message to the test reporter
        $this->signal($type, $payload);
  
        // Does a formatted print_r() for quick and dirty debugging
        $this->dump($var);
      }
    }
  ?>
  
  <?php
    /**
     * A test suite class that loads all tests from files that end
     * in "_test.php", from a directory structure like this:
     * 
     * lib-foo/test/1_test.php
     * lib-foo/test/2_test.php
     * lib-bar/test/1_test.php
     * lib-bar/test/2_test.php
     * this_class_in_a_file.php
     */
    require 'simpletest/autorun.php';
    class AllTests extends TestSuite {
      function AllTests() {
        $this->TestSuite('All tests');
  
        // Load all test files from all libs
        $glob_pattern = dirname(__FILE__) . "/**/test/*_test.php";
        $test_files   = glob($glob_pattern);
        foreach ($test_files as $test_file) {
          $this->addFile($test_file);
        }
      }
    }
  ?>
