# api documentation for  [sql (v0.75.0)](https://github.com/brianc/node-sql)  [![npm package](https://img.shields.io/npm/v/npmdoc-sql.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sql) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sql.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sql)
#### sql builder

[![NPM](https://nodei.co/npm/sql.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sql)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sql/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sql/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sql/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sql/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "brianc"
    },
    "bugs": {
        "url": "https://github.com/brianc/node-sql/issues"
    },
    "dependencies": {
        "lodash": "4.1.x",
        "sliced": "0.0.x"
    },
    "description": "sql builder",
    "devDependencies": {
        "jshint": "*",
        "mocha": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "d46e6cc062ae38e39ee68908dcb71efadfb945bd",
        "tarball": "https://registry.npmjs.org/sql/-/sql-0.75.0.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "7187f755da8dcd08a525ca3c9f5cf8e119288b11",
    "homepage": "https://github.com/brianc/node-sql",
    "license": "MIT",
    "main": "lib/",
    "maintainers": [
        {
            "name": "brianc"
        }
    ],
    "name": "sql",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/brianc/node-sql.git"
    },
    "scripts": {
        "lint": "jshint lib test",
        "posttest": "jshint lib test",
        "test": "mocha"
    },
    "version": "0.75.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sql](#apidoc.module.sql)
1.  [function <span class="apidocSignatureSpan">sql.</span>Sql (dialect, config)](#apidoc.element.sql.Sql)
1.  [function <span class="apidocSignatureSpan">sql.</span>Table (config)](#apidoc.element.sql.Table)
1.  [function <span class="apidocSignatureSpan">sql.</span>create (dialect, config)](#apidoc.element.sql.create)
1.  [function <span class="apidocSignatureSpan">sql.</span>dialect (config)](#apidoc.element.sql.dialect)
1.  object <span class="apidocSignatureSpan">sql.</span>Sql.prototype
1.  object <span class="apidocSignatureSpan">sql.</span>Table.prototype
1.  object <span class="apidocSignatureSpan">sql.</span>config
1.  object <span class="apidocSignatureSpan">sql.</span>dialect.prototype
1.  object <span class="apidocSignatureSpan">sql.</span>functions
1.  string <span class="apidocSignatureSpan">sql.</span>dialectName

#### [module sql.Sql](#apidoc.module.sql.Sql)
1.  [function <span class="apidocSignatureSpan">sql.</span>Sql (dialect, config)](#apidoc.element.sql.Sql.Sql)

#### [module sql.Sql.prototype](#apidoc.module.sql.Sql.prototype)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>array ()](#apidoc.element.sql.Sql.prototype.array)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>constant (value)](#apidoc.element.sql.Sql.prototype.constant)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>define (def)](#apidoc.element.sql.Sql.prototype.define)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>functionCallCreator (name)](#apidoc.element.sql.Sql.prototype.functionCallCreator)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>interval ()](#apidoc.element.sql.Sql.prototype.interval)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>select ()](#apidoc.element.sql.Sql.prototype.select)
1.  [function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>setDialect (dialect, config)](#apidoc.element.sql.Sql.prototype.setDialect)

#### [module sql.Table](#apidoc.module.sql.Table)
1.  [function <span class="apidocSignatureSpan">sql.</span>Table (config)](#apidoc.element.sql.Table.Table)
1.  [function <span class="apidocSignatureSpan">sql.Table.</span>define (config)](#apidoc.element.sql.Table.define)

#### [module sql.Table.prototype](#apidoc.module.sql.Table.prototype)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>addColumn (col, options)](#apidoc.element.sql.Table.prototype.addColumn)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>alter ()](#apidoc.element.sql.Table.prototype.alter)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>and ()](#apidoc.element.sql.Table.prototype.and)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>as (alias)](#apidoc.element.sql.Table.prototype.as)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>clone (config)](#apidoc.element.sql.Table.prototype.clone)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>count (alias)](#apidoc.element.sql.Table.prototype.count)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>create ()](#apidoc.element.sql.Table.prototype.create)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>createColumn (col)](#apidoc.element.sql.Table.prototype.createColumn)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>delete ()](#apidoc.element.sql.Table.prototype.delete)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>drop ()](#apidoc.element.sql.Table.prototype.drop)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>from ()](#apidoc.element.sql.Table.prototype.from)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>get (colName)](#apidoc.element.sql.Table.prototype.get)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>getColumn (colName)](#apidoc.element.sql.Table.prototype.getColumn)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>getName ()](#apidoc.element.sql.Table.prototype.getName)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>getSchema ()](#apidoc.element.sql.Table.prototype.getSchema)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>hasColumn (col)](#apidoc.element.sql.Table.prototype.hasColumn)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>indexes ()](#apidoc.element.sql.Table.prototype.indexes)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>insert ()](#apidoc.element.sql.Table.prototype.insert)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>join (other)](#apidoc.element.sql.Table.prototype.join)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>joinTo (other)](#apidoc.element.sql.Table.prototype.joinTo)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>leftJoin (other)](#apidoc.element.sql.Table.prototype.leftJoin)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>limit ()](#apidoc.element.sql.Table.prototype.limit)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>literal (literal)](#apidoc.element.sql.Table.prototype.literal)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>offset ()](#apidoc.element.sql.Table.prototype.offset)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>or ()](#apidoc.element.sql.Table.prototype.or)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>order ()](#apidoc.element.sql.Table.prototype.order)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>select ()](#apidoc.element.sql.Table.prototype.select)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>setSchema (schema)](#apidoc.element.sql.Table.prototype.setSchema)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>star (options)](#apidoc.element.sql.Table.prototype.star)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>subQuery (alias)](#apidoc.element.sql.Table.prototype.subQuery)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>toNode ()](#apidoc.element.sql.Table.prototype.toNode)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>truncate ()](#apidoc.element.sql.Table.prototype.truncate)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>update ()](#apidoc.element.sql.Table.prototype.update)
1.  [function <span class="apidocSignatureSpan">sql.Table.prototype.</span>where ()](#apidoc.element.sql.Table.prototype.where)
1.  object <span class="apidocSignatureSpan">sql.Table.prototype.</span>nodes

#### [module sql.dialect](#apidoc.module.sql.dialect)
1.  [function <span class="apidocSignatureSpan">sql.</span>dialect (config)](#apidoc.element.sql.dialect.dialect)

#### [module sql.dialect.prototype](#apidoc.module.sql.dialect.prototype)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_getParameterPlaceholder (index, value)](#apidoc.element.sql.dialect.prototype._getParameterPlaceholder)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_getParameterText (index, value)](#apidoc.element.sql.dialect.prototype._getParameterText)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_getParameterValue (value, quoteChar)](#apidoc.element.sql.dialect.prototype._getParameterValue)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_myClass (config)](#apidoc.element.sql.dialect.prototype._myClass)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>findNode (list, type)](#apidoc.element.sql.dialect.prototype.findNode)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>getQuery (queryNode)](#apidoc.element.sql.dialect.prototype.getQuery)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>getString (queryNode)](#apidoc.element.sql.dialect.prototype.getString)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>handleDistinct (actions, filters)](#apidoc.element.sql.dialect.prototype.handleDistinct)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>quote (word, quoteCharacter)](#apidoc.element.sql.dialect.prototype.quote)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visit (node)](#apidoc.element.sql.dialect.prototype.visit)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAddColumn (addColumn)](#apidoc.element.sql.dialect.prototype.visitAddColumn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAlias (alias)](#apidoc.element.sql.dialect.prototype.visitAlias)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAlter (alter)](#apidoc.element.sql.dialect.prototype.visitAlter)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitArrayCall (arrayCall)](#apidoc.element.sql.dialect.prototype.visitArrayCall)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAt (at)](#apidoc.element.sql.dialect.prototype.visitAt)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitBinary (binary)](#apidoc.element.sql.dialect.prototype.visitBinary)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCascade ()](#apidoc.element.sql.dialect.prototype.visitCascade)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCase (caseExp)](#apidoc.element.sql.dialect.prototype.visitCase)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCast (cast)](#apidoc.element.sql.dialect.prototype.visitCast)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitColumn (columnNode)](#apidoc.element.sql.dialect.prototype.visitColumn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitContainedBy (containedBy)](#apidoc.element.sql.dialect.prototype.visitContainedBy)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitContains (contains)](#apidoc.element.sql.dialect.prototype.visitContains)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCreate (create)](#apidoc.element.sql.dialect.prototype.visitCreate)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCreateIndex (node)](#apidoc.element.sql.dialect.prototype.visitCreateIndex)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCreateView (createView)](#apidoc.element.sql.dialect.prototype.visitCreateView)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDefault (parameter)](#apidoc.element.sql.dialect.prototype.visitDefault)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDelete (del)](#apidoc.element.sql.dialect.prototype.visitDelete)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDistinct (truncate)](#apidoc.element.sql.dialect.prototype.visitDistinct)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDistinctOn (distinctOn)](#apidoc.element.sql.dialect.prototype.visitDistinctOn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDrop (drop)](#apidoc.element.sql.dialect.prototype.visitDrop)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDropColumn (dropColumn)](#apidoc.element.sql.dialect.prototype.visitDropColumn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDropIndex (node)](#apidoc.element.sql.dialect.prototype.visitDropIndex)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitForShare ()](#apidoc.element.sql.dialect.prototype.visitForShare)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitForUpdate ()](#apidoc.element.sql.dialect.prototype.visitForUpdate)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitForeignKey (foreignKeyNode)](#apidoc.element.sql.dialect.prototype.visitForeignKey)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitFrom (from)](#apidoc.element.sql.dialect.prototype.visitFrom)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitFunctionCall (functionCall)](#apidoc.element.sql.dialect.prototype.visitFunctionCall)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitGroupBy (groupBy)](#apidoc.element.sql.dialect.prototype.visitGroupBy)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitHaving (having)](#apidoc.element.sql.dialect.prototype.visitHaving)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIfExists ()](#apidoc.element.sql.dialect.prototype.visitIfExists)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIfNotExists ()](#apidoc.element.sql.dialect.prototype.visitIfNotExists)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIn (binary)](#apidoc.element.sql.dialect.prototype.visitIn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIndexes (node)](#apidoc.element.sql.dialect.prototype.visitIndexes)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitInsert (insert)](#apidoc.element.sql.dialect.prototype.visitInsert)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitInterval (interval)](#apidoc.element.sql.dialect.prototype.visitInterval)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitJoin (join)](#apidoc.element.sql.dialect.prototype.visitJoin)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitLiteral (node)](#apidoc.element.sql.dialect.prototype.visitLiteral)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitModifier (node)](#apidoc.element.sql.dialect.prototype.visitModifier)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitNotIn (binary)](#apidoc.element.sql.dialect.prototype.visitNotIn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOnConflict (onConflict)](#apidoc.element.sql.dialect.prototype.visitOnConflict)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOnDuplicate (onDuplicate)](#apidoc.element.sql.dialect.prototype.visitOnDuplicate)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOrIgnore ()](#apidoc.element.sql.dialect.prototype.visitOrIgnore)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOrderBy (orderBy)](#apidoc.element.sql.dialect.prototype.visitOrderBy)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOrderByValue (orderByValue)](#apidoc.element.sql.dialect.prototype.visitOrderByValue)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOverlap (overlap)](#apidoc.element.sql.dialect.prototype.visitOverlap)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitParameter (parameter)](#apidoc.element.sql.dialect.prototype.visitParameter)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitPostfixUnary (unary)](#apidoc.element.sql.dialect.prototype.visitPostfixUnary)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitPrefixUnary (unary)](#apidoc.element.sql.dialect.prototype.visitPrefixUnary)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitQuery (queryNode)](#apidoc.element.sql.dialect.prototype.visitQuery)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitQueryHelper (actions, targets, filters)](#apidoc.element.sql.dialect.prototype.visitQueryHelper)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitRename (rename)](#apidoc.element.sql.dialect.prototype.visitRename)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitRenameColumn (renameColumn)](#apidoc.element.sql.dialect.prototype.visitRenameColumn)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitRestrict ()](#apidoc.element.sql.dialect.prototype.visitRestrict)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitReturning (returning)](#apidoc.element.sql.dialect.prototype.visitReturning)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitSelect (select)](#apidoc.element.sql.dialect.prototype.visitSelect)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitSlice (slice)](#apidoc.element.sql.dialect.prototype.visitSlice)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitSubquery (queryNode, dontParenthesize)](#apidoc.element.sql.dialect.prototype.visitSubquery)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitTable (tableNode)](#apidoc.element.sql.dialect.prototype.visitTable)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitTernary (ternary)](#apidoc.element.sql.dialect.prototype.visitTernary)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitTruncate (truncate)](#apidoc.element.sql.dialect.prototype.visitTruncate)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitUpdate (update)](#apidoc.element.sql.dialect.prototype.visitUpdate)
1.  [function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitWhere (where)](#apidoc.element.sql.dialect.prototype.visitWhere)
1.  string <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_aliasText
1.  string <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_arrayAggFunctionName
1.  string <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_quoteCharacter

#### [module sql.functions](#apidoc.module.sql.functions)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>ABS ()](#apidoc.element.sql.functions.ABS)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>AVG ()](#apidoc.element.sql.functions.AVG)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>COALESCE ()](#apidoc.element.sql.functions.COALESCE)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>COUNT ()](#apidoc.element.sql.functions.COUNT)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>CURRENT_TIMESTAMP ()](#apidoc.element.sql.functions.CURRENT_TIMESTAMP)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>DAY ()](#apidoc.element.sql.functions.DAY)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>DISTINCT ()](#apidoc.element.sql.functions.DISTINCT)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>HOUR ()](#apidoc.element.sql.functions.HOUR)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>HSTORE ()](#apidoc.element.sql.functions.HSTORE)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>LEFT ()](#apidoc.element.sql.functions.LEFT)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>LENGTH ()](#apidoc.element.sql.functions.LENGTH)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>LOWER ()](#apidoc.element.sql.functions.LOWER)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>LTRIM ()](#apidoc.element.sql.functions.LTRIM)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>MAX ()](#apidoc.element.sql.functions.MAX)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>MIN ()](#apidoc.element.sql.functions.MIN)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>MONTH ()](#apidoc.element.sql.functions.MONTH)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>PLAINTO_TSQUERY ()](#apidoc.element.sql.functions.PLAINTO_TSQUERY)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>RANDOM ()](#apidoc.element.sql.functions.RANDOM)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>RIGHT ()](#apidoc.element.sql.functions.RIGHT)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>ROUND ()](#apidoc.element.sql.functions.ROUND)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>RTRIM ()](#apidoc.element.sql.functions.RTRIM)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>SETWEIGHT ()](#apidoc.element.sql.functions.SETWEIGHT)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>SUBSTR ()](#apidoc.element.sql.functions.SUBSTR)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>SUM ()](#apidoc.element.sql.functions.SUM)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>TO_TSQUERY ()](#apidoc.element.sql.functions.TO_TSQUERY)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>TO_TSVECTOR ()](#apidoc.element.sql.functions.TO_TSVECTOR)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>TRIM ()](#apidoc.element.sql.functions.TRIM)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>TS_RANK ()](#apidoc.element.sql.functions.TS_RANK)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>TS_RANK_CD ()](#apidoc.element.sql.functions.TS_RANK_CD)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>UPPER ()](#apidoc.element.sql.functions.UPPER)
1.  [function <span class="apidocSignatureSpan">sql.functions.</span>YEAR ()](#apidoc.element.sql.functions.YEAR)



# <a name="apidoc.module.sql"></a>[module sql](#apidoc.module.sql)

#### <a name="apidoc.element.sql.Sql"></a>[function <span class="apidocSignatureSpan">sql.</span>Sql (dialect, config)](#apidoc.element.sql.Sql)
- description and source-code
```javascript
Sql = function (dialect, config) {
  this.setDialect(dialect || DEFAULT_DIALECT, config);

  // attach the standard SQL functions to this instance
  this.functions = functions.getStandardFunctions();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table"></a>[function <span class="apidocSignatureSpan">sql.</span>Table (config)](#apidoc.element.sql.Table)
- description and source-code
```javascript
Table = function (config) {
  this._schema = config.schema;
  this._name = config.name;
  this._initialConfig = config;
  this.columnWhiteList = !!config.columnWhiteList;
  this.isTemporary=!!config.isTemporary;
  this.snakeToCamel = !!config.snakeToCamel;
  this.columns = [];
  this.foreignKeys = [];
  this.table = this;
  if (!config.sql) {
    config.sql = require('./index');
  }
  this.sql = config.sql;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.create"></a>[function <span class="apidocSignatureSpan">sql.</span>create (dialect, config)](#apidoc.element.sql.create)
- description and source-code
```javascript
create = function (dialect, config) {
  return new Sql(dialect, {});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect"></a>[function <span class="apidocSignatureSpan">sql.</span>dialect (config)](#apidoc.element.sql.dialect)
- description and source-code
```javascript
dialect = function (config) {
  this.output = [];
  this.params = [];
  this.config = config || {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sql.Sql"></a>[module sql.Sql](#apidoc.module.sql.Sql)

#### <a name="apidoc.element.sql.Sql.Sql"></a>[function <span class="apidocSignatureSpan">sql.</span>Sql (dialect, config)](#apidoc.element.sql.Sql.Sql)
- description and source-code
```javascript
Sql = function (dialect, config) {
  this.setDialect(dialect || DEFAULT_DIALECT, config);

  // attach the standard SQL functions to this instance
  this.functions = functions.getStandardFunctions();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sql.Sql.prototype"></a>[module sql.Sql.prototype](#apidoc.module.sql.Sql.prototype)

#### <a name="apidoc.element.sql.Sql.prototype.array"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>array ()](#apidoc.element.sql.Sql.prototype.array)
- description and source-code
```javascript
array = function () {
  var arrayCall = new ArrayCall(sliced(arguments));
  arrayCall.sql = this;
  return arrayCall;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Sql.prototype.constant"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>constant (value)](#apidoc.element.sql.Sql.prototype.constant)
- description and source-code
```javascript
constant = function (value) {
  var config={
    name:"constant",
    property:"constant",
    isConstant:true,
    constantValue:value,
  };
  var cn = new Column(config);
  return cn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Sql.prototype.define"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>define (def)](#apidoc.element.sql.Sql.prototype.define)
- description and source-code
```javascript
define = function (def) {
  def = _.defaults(def || {}, {
    sql: this
  });

  return Table.define(def);
}
```
- example usage
```shell
...
var sql = require('sql');

//(optionally) set the SQL dialect
sql.setDialect('postgres');
//possible dialects: mssql, mysql, postgres (default), sqlite

//first we define our tables
var user = sql.define({
name: 'user',
columns: ['id', 'name', 'email', 'lastLogin']
});

var post = sql.define({
name: 'post',
columns: ['id', 'userId', 'date', 'title', 'body']
...
```

#### <a name="apidoc.element.sql.Sql.prototype.functionCallCreator"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>functionCallCreator (name)](#apidoc.element.sql.Sql.prototype.functionCallCreator)
- description and source-code
```javascript
functionCallCreator = function (name) {
  return function() {
    return new FunctionCall(name, sliced(arguments));
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Sql.prototype.interval"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>interval ()](#apidoc.element.sql.Sql.prototype.interval)
- description and source-code
```javascript
interval = function () {
  var interval = new Interval(sliced(arguments));
  return interval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Sql.prototype.select"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>select ()](#apidoc.element.sql.Sql.prototype.select)
- description and source-code
```javascript
select = function () {
  var query = new Query({sql: this});
  query.select.apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

var post = sql.define({
  name: 'post',
  columns: ['id', 'userId', 'date', 'title', 'body']
});

//now let's make a simple query
var query = user.select(user.star()).from(user).toQuery();
console.log(query.text); //SELECT "user".* FROM "user"

//something more interesting
var query = user
.select(user.id)
.from(user)
.where(
...
```

#### <a name="apidoc.element.sql.Sql.prototype.setDialect"></a>[function <span class="apidocSignatureSpan">sql.Sql.prototype.</span>setDialect (dialect, config)](#apidoc.element.sql.Sql.prototype.setDialect)
- description and source-code
```javascript
setDialect = function (dialect, config) {
  this.dialect     = getDialect(dialect);
  this.dialectName = dialect;
  this.config      = config;

  return this;
}
```
- example usage
```shell
...
## use

'''js
//require the module
var sql = require('sql');

//(optionally) set the SQL dialect
sql.setDialect('postgres');
//possible dialects: mssql, mysql, postgres (default), sqlite

//first we define our tables
var user = sql.define({
  name: 'user',
  columns: ['id', 'name', 'email', 'lastLogin']
});
...
```



# <a name="apidoc.module.sql.Table"></a>[module sql.Table](#apidoc.module.sql.Table)

#### <a name="apidoc.element.sql.Table.Table"></a>[function <span class="apidocSignatureSpan">sql.</span>Table (config)](#apidoc.element.sql.Table.Table)
- description and source-code
```javascript
Table = function (config) {
  this._schema = config.schema;
  this._name = config.name;
  this._initialConfig = config;
  this.columnWhiteList = !!config.columnWhiteList;
  this.isTemporary=!!config.isTemporary;
  this.snakeToCamel = !!config.snakeToCamel;
  this.columns = [];
  this.foreignKeys = [];
  this.table = this;
  if (!config.sql) {
    config.sql = require('./index');
  }
  this.sql = config.sql;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.define"></a>[function <span class="apidocSignatureSpan">sql.Table.</span>define (config)](#apidoc.element.sql.Table.define)
- description and source-code
```javascript
define = function (config) {
  var table = new Table(config);
  // allow hash of columns as well as array
  if (config.columns && !util.isArray(config.columns)) {
    var cols = [];

    for (var key in config.columns) {
      if (config.columns.hasOwnProperty(key)) {
        var col = config.columns[key];
        col.name = key;
        cols.push(col);
      }
    }

    config.columns = cols;
  }

  for (var i = 0; i < config.columns.length; i++) {
    table.addColumn(config.columns[i]);
  }

  if(config.foreignKeys !== undefined) {
    if(util.isArray(config.foreignKeys)) {
      for(i = 0; i < config.foreignKeys.length; i++) {
        table.foreignKeys.push(new ForeignKeyNode(config.foreignKeys[i]));
      }
    } else {
      table.foreignKeys.push(new ForeignKeyNode(config.foreignKeys));
    }
  }
  return table;
}
```
- example usage
```shell
...
var sql = require('sql');

//(optionally) set the SQL dialect
sql.setDialect('postgres');
//possible dialects: mssql, mysql, postgres (default), sqlite

//first we define our tables
var user = sql.define({
name: 'user',
columns: ['id', 'name', 'email', 'lastLogin']
});

var post = sql.define({
name: 'post',
columns: ['id', 'userId', 'date', 'title', 'body']
...
```



# <a name="apidoc.module.sql.Table.prototype"></a>[module sql.Table.prototype](#apidoc.module.sql.Table.prototype)

#### <a name="apidoc.element.sql.Table.prototype.addColumn"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>addColumn (col, options)](#apidoc.element.sql.Table.prototype.addColumn)
- description and source-code
```javascript
addColumn = function (col, options) {
  col     = this.createColumn(col);
  options = lodash.extend({
    noisy: true
  }, options || {});

  if(this.hasColumn(col)) {
    if (options.noisy) {
      throw new Error('Table ' + this._name + ' already has column or property by the name of ' + col.name);
    } else {
      return this;
    }
  } else if(!!this[col.name] && (process.env.NODE_ENV === 'debug')) {
    console.log('Please notice that you have just defined the column "' + col.name + '". In order to access it, you need to use "
table.getColumn(\'' + col.name + '\');"!');
  }
  this.columns.push(col);

  function snakeToCamel(snakeName) {
    return snakeName.replace(/[\-_]([a-z])/g, function(m, $1){ return $1.toUpperCase(); });
  }

  var property = col.property = col.property || (this.snakeToCamel ? snakeToCamel(col.name) : col.name);
  this[property] = this[property] || col;
  return this;
}
```
- example usage
```shell
...
    ]
});

/**
 * Adding a column to an existing table:
 */
var model = sql.define({ name: 'foo', columns: [] });
model.addColumn('id');

// If you try to add another column "id", node-sql will throw an error.
// You can suppress that error via:
model.addColumn('id', { noisy: false });
'''

Read the module's documentation for more details.
...
```

#### <a name="apidoc.element.sql.Table.prototype.alter"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>alter ()](#apidoc.element.sql.Table.prototype.alter)
- description and source-code
```javascript
alter = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.and"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>and ()](#apidoc.element.sql.Table.prototype.and)
- description and source-code
```javascript
and = function () {
  var query = new Query(this);
  query.where.apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
console.log(query.text); //SELECT "user".* FROM "user"

//something more interesting
var query = user
    .select(user.id)
    .from(user)
    .where(
      user.name.equals('boom').and(user.id.equals(1))
    ).or(
      user.name.equals('bang').and(user.id.equals(2))
    ).toQuery();

//query is parameterized by default
console.log(query.text); //SELECT "user"."id" FROM "user" WHERE ((("user"."name" = $1) AND ("user"."id" = $2)) OR (("user"."name
" = $3) AND ("user"."id" = $4)))
...
```

#### <a name="apidoc.element.sql.Table.prototype.as"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>as (alias)](#apidoc.element.sql.Table.prototype.as)
- description and source-code
```javascript
as = function (alias) {
  // TODO could this be cleaner?
  var t = Table.define(this._initialConfig);
  t.alias = alias;
  return t;
}
```
- example usage
```shell
...
//this also makes parts of your queries composable, which is handy

var friendship = sql.define({
  name: 'friendship',
  columns: ['userId', 'friendId']
});

var friends = user.as('friends');
var userToFriends = user
  .leftJoin(friendship).on(user.id.equals(friendship.userId))
  .leftJoin(friends).on(friendship.friendId.equals(friends.id));

//and now...compose...
var friendsWhoHaveLoggedInQuery = user.from(userToFriends).where(friends.lastLogin.isNotNull());
//SELECT * FROM "user"
...
```

#### <a name="apidoc.element.sql.Table.prototype.clone"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>clone (config)](#apidoc.element.sql.Table.prototype.clone)
- description and source-code
```javascript
clone = function (config) {
  return Table.define(lodash.extend({
    schema: this._schema,
    name: this._name,
    sql: this.sql,
    columnWhiteList: !!this.columnWhiteList,
    snakeToCamel: !!this.snakeToCamel,
    columns: this.columns,
    foreignKeys: this.foreignKeys
  }, config || {}));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.count"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>count (alias)](#apidoc.element.sql.Table.prototype.count)
- description and source-code
```javascript
count = function (alias) {
  var name = this.alias || this._name,
    col = new Column({table: this, star: true});
  // ColumnNode
  return col.count(alias || name + '_count');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.create"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>create ()](#apidoc.element.sql.Table.prototype.create)
- description and source-code
```javascript
create = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.createColumn"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>createColumn (col)](#apidoc.element.sql.Table.prototype.createColumn)
- description and source-code
```javascript
createColumn = function (col) {
  if(!(col instanceof Column)) {
    if(typeof col === 'string') {
      col = { name: col };
    }

    col.table = this;
    col = new Column(col);

    // Load subfields from array into an object of form name: Column
    if(util.isArray(col.subfields)) {
      col.subfields = lodash.chain(col.subfields)
        .map(lodash.bind(function (subfield) {
          return [subfield, new Column({
            table: this,
            subfieldContainer: col,
            name: subfield
          })];
        }, this))
        .fromPairs()
        .value();
    }
  }

  return col;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.delete"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>delete ()](#apidoc.element.sql.Table.prototype.delete)
- description and source-code
```javascript
delete = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.drop"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>drop ()](#apidoc.element.sql.Table.prototype.drop)
- description and source-code
```javascript
drop = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.from"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>from ()](#apidoc.element.sql.Table.prototype.from)
- description and source-code
```javascript
from = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

var post = sql.define({
  name: 'post',
  columns: ['id', 'userId', 'date', 'title', 'body']
});

//now let's make a simple query
var query = user.select(user.star()).from(user).toQuery();
console.log(query.text); //SELECT "user".* FROM "user"

//something more interesting
var query = user
.select(user.id)
.from(user)
.where(
...
```

#### <a name="apidoc.element.sql.Table.prototype.get"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>get (colName)](#apidoc.element.sql.Table.prototype.get)
- description and source-code
```javascript
get = function (colName) {
  for(var i = 0; i < this.columns.length; i++) {
    var col = this.columns[i];
    if (colName === col.property || colName === col.name) {
      return col;
    }
  }
  if(this.columnWhiteList)
    return null;
  throw new Error('Table ' + this._name + ' does not have a column or property named ' + colName);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.getColumn"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>getColumn (colName)](#apidoc.element.sql.Table.prototype.getColumn)
- description and source-code
```javascript
getColumn = function (colName) {
  for(var i = 0; i < this.columns.length; i++) {
    var col = this.columns[i];
    if (colName === col.property || colName === col.name) {
      return col;
    }
  }
  if(this.columnWhiteList)
    return null;
  throw new Error('Table ' + this._name + ' does not have a column or property named ' + colName);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.getName"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>getName ()](#apidoc.element.sql.Table.prototype.getName)
- description and source-code
```javascript
getName = function () {
  if (this.sql && this.sql.dialectName=="mssql" && this.isTemporary) return "#"+this._name;
  return this._name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.getSchema"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>getSchema ()](#apidoc.element.sql.Table.prototype.getSchema)
- description and source-code
```javascript
getSchema = function () {
  return this._schema;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.hasColumn"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>hasColumn (col)](#apidoc.element.sql.Table.prototype.hasColumn)
- description and source-code
```javascript
hasColumn = function (col) {
  var columnName = col instanceof Column ? col.name : col;
  return this.columns.some(function(column) {
    return column.property === columnName || column.name === columnName;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.indexes"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>indexes ()](#apidoc.element.sql.Table.prototype.indexes)
- description and source-code
```javascript
indexes = function () {
  return new Query(this).indexes();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.insert"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>insert ()](#apidoc.element.sql.Table.prototype.insert)
- description and source-code
```javascript
insert = function () {
  var query = new Query(this);
  if(!arguments[0] || (util.isArray(arguments[0]) && arguments[0].length === 0)){
    query.select.call(query, this.star());
    query.where.apply(query,["1=2"]);
  } else {
    query.insert.apply(query, arguments);
  }
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.join"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>join (other)](#apidoc.element.sql.Table.prototype.join)
- description and source-code
```javascript
join = function (other) {
  return new JoinNode('INNER', this.toNode(), other.toNode(), other);
}
```
- example usage
```shell
...

//queries can be named
var query = user.select(user.star()).from(user).toNamedQuery('user.all');
console.log(query.name); //'user.all'

//how about a join?
var query = user.select(user.name, post.body)
.from(user.join(post).on(user.id.equals(post.userId))).toQuery();

console.log(query.text); //'SELECT "user"."name", "post"."body" FROM "user" INNER JOIN "post" ON ("user"."id" = "post"."userId")'

//this also makes parts of your queries composable, which is handy

var friendship = sql.define({
name: 'friendship',
...
```

#### <a name="apidoc.element.sql.Table.prototype.joinTo"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>joinTo (other)](#apidoc.element.sql.Table.prototype.joinTo)
- description and source-code
```javascript
joinTo = function (other) {
  return Joiner.leftJoin(this, other);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.leftJoin"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>leftJoin (other)](#apidoc.element.sql.Table.prototype.leftJoin)
- description and source-code
```javascript
leftJoin = function (other) {
  return new JoinNode('LEFT', this.toNode(), other.toNode());
}
```
- example usage
```shell
...
var friendship = sql.define({
  name: 'friendship',
  columns: ['userId', 'friendId']
});

var friends = user.as('friends');
var userToFriends = user
  .leftJoin(friendship).on(user.id.equals(friendship.userId))
  .leftJoin(friends).on(friendship.friendId.equals(friends.id));

//and now...compose...
var friendsWhoHaveLoggedInQuery = user.from(userToFriends).where(friends.lastLogin.isNotNull());
//SELECT * FROM "user"
//LEFT JOIN "friendship" ON ("user"."id" = "friendship"."userId")
//LEFT JOIN "user" AS "friends" ON ("friendship"."friendId" = "friends"."id")
...
```

#### <a name="apidoc.element.sql.Table.prototype.limit"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>limit ()](#apidoc.element.sql.Table.prototype.limit)
- description and source-code
```javascript
limit = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.literal"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>literal (literal)](#apidoc.element.sql.Table.prototype.literal)
- description and source-code
```javascript
literal = function (literal) {
  return new LiteralNode(literal);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.offset"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>offset ()](#apidoc.element.sql.Table.prototype.offset)
- description and source-code
```javascript
offset = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.or"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>or ()](#apidoc.element.sql.Table.prototype.or)
- description and source-code
```javascript
or = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

//something more interesting
var query = user
    .select(user.id)
    .from(user)
    .where(
      user.name.equals('boom').and(user.id.equals(1))
    ).or(
      user.name.equals('bang').and(user.id.equals(2))
    ).toQuery();

//query is parameterized by default
console.log(query.text); //SELECT "user"."id" FROM "user" WHERE ((("user"."name" = $1) AND ("user"."id" = $2)) OR (("user"."name
" = $3) AND ("user"."id" = $4)))

console.log(query.values); //['boom', 1, 'bang', 2]
...
```

#### <a name="apidoc.element.sql.Table.prototype.order"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>order ()](#apidoc.element.sql.Table.prototype.order)
- description and source-code
```javascript
order = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.select"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>select ()](#apidoc.element.sql.Table.prototype.select)
- description and source-code
```javascript
select = function () {
  // create the query and pass it off
  var query = new Query(this);
  if (arguments.length === 0) {
    query.select.call(query, this.star());
  } else {
    query.select.apply(query, arguments);
  }
  return query;
}
```
- example usage
```shell
...

var post = sql.define({
  name: 'post',
  columns: ['id', 'userId', 'date', 'title', 'body']
});

//now let's make a simple query
var query = user.select(user.star()).from(user).toQuery();
console.log(query.text); //SELECT "user".* FROM "user"

//something more interesting
var query = user
.select(user.id)
.from(user)
.where(
...
```

#### <a name="apidoc.element.sql.Table.prototype.setSchema"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>setSchema (schema)](#apidoc.element.sql.Table.prototype.setSchema)
- description and source-code
```javascript
setSchema = function (schema) {
  this._schema = schema;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.star"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>star (options)](#apidoc.element.sql.Table.prototype.star)
- description and source-code
```javascript
star = function (options) {
  options = options || {};
  if (options.prefix) {
    return this.columns.map(function(column) {
      return this[column.name].as(options.prefix + column.name);
    }.bind(this));
  }

  return new Column({table: this, star: true});
}
```
- example usage
```shell
...

var post = sql.define({
  name: 'post',
  columns: ['id', 'userId', 'date', 'title', 'body']
});

//now let's make a simple query
var query = user.select(user.star()).from(user).toQuery();
console.log(query.text); //SELECT "user".* FROM "user"

//something more interesting
var query = user
.select(user.id)
.from(user)
.where(
...
```

#### <a name="apidoc.element.sql.Table.prototype.subQuery"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>subQuery (alias)](#apidoc.element.sql.Table.prototype.subQuery)
- description and source-code
```javascript
subQuery = function (alias) {
  // create the query and pass it off
  var query = new Query(this);
  query.type = 'SUBQUERY';
  query.alias = alias;
  query.join = function(other) {
    return new JoinNode('INNER', this.toNode(), other.toNode(), other);
  };
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.toNode"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>toNode ()](#apidoc.element.sql.Table.prototype.toNode)
- description and source-code
```javascript
toNode = function () {
  return new TableNode(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.truncate"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>truncate ()](#apidoc.element.sql.Table.prototype.truncate)
- description and source-code
```javascript
truncate = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.update"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>update ()](#apidoc.element.sql.Table.prototype.update)
- description and source-code
```javascript
update = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.Table.prototype.where"></a>[function <span class="apidocSignatureSpan">sql.Table.prototype.</span>where ()](#apidoc.element.sql.Table.prototype.where)
- description and source-code
```javascript
where = function () {
  var query = new Query(this);
  query[method].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
var query = user.select(user.star()).from(user).toQuery();
console.log(query.text); //SELECT "user".* FROM "user"

//something more interesting
var query = user
    .select(user.id)
    .from(user)
    .where(
      user.name.equals('boom').and(user.id.equals(1))
    ).or(
      user.name.equals('bang').and(user.id.equals(2))
    ).toQuery();

//query is parameterized by default
console.log(query.text); //SELECT "user"."id" FROM "user" WHERE ((("user"."name" = $1) AND ("user"."id" = $2)) OR (("user"."name
" = $3) AND ("user"."id" = $4)))
...
```



# <a name="apidoc.module.sql.dialect"></a>[module sql.dialect](#apidoc.module.sql.dialect)

#### <a name="apidoc.element.sql.dialect.dialect"></a>[function <span class="apidocSignatureSpan">sql.</span>dialect (config)](#apidoc.element.sql.dialect.dialect)
- description and source-code
```javascript
dialect = function (config) {
  this.output = [];
  this.params = [];
  this.config = config || {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sql.dialect.prototype"></a>[module sql.dialect.prototype](#apidoc.module.sql.dialect.prototype)

#### <a name="apidoc.element.sql.dialect.prototype._getParameterPlaceholder"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_getParameterPlaceholder (index, value)](#apidoc.element.sql.dialect.prototype._getParameterPlaceholder)
- description and source-code
```javascript
_getParameterPlaceholder = function (index, value) {
<span class="apidocCodeCommentSpan">  /* jshint unused: false */
</span>  return '$' + index;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype._getParameterText"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_getParameterText (index, value)](#apidoc.element.sql.dialect.prototype._getParameterText)
- description and source-code
```javascript
_getParameterText = function (index, value) {
  if (this._disableParameterPlaceholders) {
    // do not use placeholder
    return this._getParameterValue(value);
  } else {
    // use placeholder
    return this._getParameterPlaceholder(index, value);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype._getParameterValue"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_getParameterValue (value, quoteChar)](#apidoc.element.sql.dialect.prototype._getParameterValue)
- description and source-code
```javascript
_getParameterValue = function (value, quoteChar) {
  // handle primitives
  if (null === value) {
    value = 'NULL';
  } else if ('boolean' === typeof value) {
    value = value ? 'TRUE' : 'FALSE';
  } else if ('number' === typeof value) {
    // number is just number
    value = value;
  } else if ('string' === typeof value) {
    // string uses single quote by default
    value = this.quote(value, quoteChar || "'");
  } else if ('object' === typeof value) {
    if (Array.isArray(value)) {
      if (this._myClass === Postgres) {
        // naive check to see if this is an array of objects, which
        // is handled differently than an array of primitives
        if (value.length && 'object' === typeof value[0] &&
            !_.isFunction(value[0].toISOString) &&
            !Array.isArray(value[0])) {
            value = "'" + JSON.stringify(value) + "'";
        } else {
            var self = this;
            value = value.map(function (item) {
                // In a Postgres array, strings must be double-quoted
                return self._getParameterValue(item, '"');
            });
            value = '\'{' + value.join(',') + '}\'';
        }
      } else {
        value = _.map(value, this._getParameterValue.bind(this));
        value = '(' + value.join(', ') + ')';
      }
    } else if (value instanceof Date) {
      // Date object's default toString format does not get parsed well
      // Handle dates using toISOString
      value = this._getParameterValue(value.toISOString());
    } else if (Buffer.isBuffer(value)) {
      value = this._getParameterValue('\\x' + value.toString('hex'));
    } else {
      // rich object represent with string
      var strValue = value.toString();
      value = strValue === '[object Object]' ? this._getParameterValue(JSON.stringify(value)) : this._getParameterValue(strValue
);
    }
  } else {
    throw new Error('Unable to use ' + value + ' in query');
  }

  // value has been converted at this point
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype._myClass"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>_myClass (config)](#apidoc.element.sql.dialect.prototype._myClass)
- description and source-code
```javascript
_myClass = function (config) {
  this.output = [];
  this.params = [];
  this.config = config || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.findNode"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>findNode (list, type)](#apidoc.element.sql.dialect.prototype.findNode)
- description and source-code
```javascript
findNode = function (list, type) {
  for (var i= 0, len=list.length; i<len; i++) {
    var n=list[i];
    if (n.type==type) return {index:i,node:n};
  }
  return undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.getQuery"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>getQuery (queryNode)](#apidoc.element.sql.dialect.prototype.getQuery)
- description and source-code
```javascript
getQuery = function (queryNode) {
  // passed in a table, not a query
  if (queryNode instanceof Table) {
    queryNode = queryNode.select(queryNode.star());
  }
  this.output = this.visit(queryNode);

  //if is a create view, must replace paramaters with values
  if (this.output.indexOf('CREATE VIEW') > -1) {
    var previousFlagStatus = this._disableParameterPlaceholders;
    this._disableParameterPlaceholders = true;
    this.output = [];
    this.output = this.visit(queryNode);
    this.params = [];
    this._disableParameterPlaceholders = previousFlagStatus;
  }

  // create the query object
  var query = { text: this.output.join(' '), values: this.params };

  // reset the internal state of this builder
  this.output = [];
  this.params = [];

  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.getString"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>getString (queryNode)](#apidoc.element.sql.dialect.prototype.getString)
- description and source-code
```javascript
getString = function (queryNode) {
  // switch off parameter placeholders
  var previousFlagStatus = this._disableParameterPlaceholders;
  this._disableParameterPlaceholders = true;
  var query;
  try {
    // use the same code path for query building
    query = this.getQuery(queryNode);
  } finally {
    // always restore the flag afterwards
    this._disableParameterPlaceholders = previousFlagStatus;
  }
  return query.text;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.handleDistinct"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>handleDistinct (actions, filters)](#apidoc.element.sql.dialect.prototype.handleDistinct)
- description and source-code
```javascript
handleDistinct = function (actions, filters) {
  var distinctNode = this.findNode(filters,"DISTINCT");
  //if (!distinctNode) distinctNode = _findNode(targets,"DISTINCT");
  //if (!distinctNode) distinctNode = _findNode(actions,"DISTINCT");
  if (!distinctNode) return;
  var selectInfo = this.findNode(actions,"SELECT");
  if (!selectInfo) return; // there should be one by now, I think
  // mark the SELECT node that it's distinct
  selectInfo.node.isDistinct = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.quote"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>quote (word, quoteCharacter)](#apidoc.element.sql.dialect.prototype.quote)
- description and source-code
```javascript
quote = function (word, quoteCharacter) {
  var q;
  if (quoteCharacter) {
    // use the specified quote character if given
    q = quoteCharacter;
  } else {
    q = this._quoteCharacter;
  }
  // handle square brackets specially
  if (q=='['){
    return '['+word+']';
  } else {
    return q + word.replace(new RegExp(q,'g'),q+q) + q;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visit"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visit (node)](#apidoc.element.sql.dialect.prototype.visit)
- description and source-code
```javascript
visit = function (node) {
  switch(node.type) {
    case 'QUERY'           : return this.visitQuery(node);
    case 'SUBQUERY'        : return this.visitSubquery(node);
    case 'SELECT'          : return this.visitSelect(node);
    case 'INSERT'          : return this.visitInsert(node);
    case 'UPDATE'          : return this.visitUpdate(node);
    case 'DELETE'          : return this.visitDelete(node);
    case 'CREATE'          : return this.visitCreate(node);
    case 'DROP'            : return this.visitDrop(node);
    case 'TRUNCATE'        : return this.visitTruncate(node);
    case 'DISTINCT'        : return this.visitDistinct(node);
    case 'DISTINCT ON'     : return this.visitDistinctOn(node);
    case 'ALIAS'           : return this.visitAlias(node);
    case 'ALTER'           : return this.visitAlter(node);
    case 'CAST'            : return this.visitCast(node);
    case 'FROM'            : return this.visitFrom(node);
    case 'WHERE'           : return this.visitWhere(node);
    case 'ORDER BY'        : return this.visitOrderBy(node);
    case 'ORDER BY VALUE'  : return this.visitOrderByValue(node);
    case 'GROUP BY'        : return this.visitGroupBy(node);
    case 'HAVING'          : return this.visitHaving(node);
    case 'RETURNING'       : return this.visitReturning(node);
    case 'ONDUPLICATE'     : return this.visitOnDuplicate(node);
    case 'ONCONFLICT'      : return this.visitOnConflict(node);
    case 'FOR UPDATE'      : return this.visitForUpdate();
    case 'FOR SHARE'       : return this.visitForShare();
    case 'TABLE'           : return this.visitTable(node);
    case 'COLUMN'          : return this.visitColumn(node);
    case 'FOREIGN KEY'     : return this.visitForeignKey(node);
    case 'JOIN'            : return this.visitJoin(node);
    case 'LITERAL'         : return this.visitLiteral(node);
    case 'TEXT'            : return node.text;
    case 'PARAMETER'       : return this.visitParameter(node);
    case 'DEFAULT'         : return this.visitDefault(node);
    case 'IF EXISTS'       : return this.visitIfExists();
    case 'IF NOT EXISTS'   : return this.visitIfNotExists();
    case 'OR IGNORE'       : return this.visitOrIgnore();
    case 'CASCADE'         : return this.visitCascade();
    case 'RESTRICT'        : return this.visitRestrict();
    case 'RENAME'          : return this.visitRename(node);
    case 'ADD COLUMN'      : return this.visitAddColumn(node);
    case 'DROP COLUMN'     : return this.visitDropColumn(node);
    case 'RENAME COLUMN'   : return this.visitRenameColumn(node);
    case 'INDEXES'         : return this.visitIndexes(node);
    case 'CREATE INDEX'    : return this.visitCreateIndex(node);
    case 'DROP INDEX'      : return this.visitDropIndex(node);
    case 'FUNCTION CALL'   : return this.visitFunctionCall(node);
    case 'ARRAY CALL'      : return this.visitArrayCall(node);
    case 'CREATE VIEW'     : return this.visitCreateView(node);
    case 'INTERVAL'        : return this.visitInterval(node);

    case 'POSTFIX UNARY' : return this.visitPostfixUnary(node);
    case 'PREFIX UNARY'  : return this.visitPrefixUnary(node);
    case 'BINARY'        : return this.visitBinary(node);
    case 'TERNARY'       : return this.visitTernary(node);
    case 'IN'            : return this.visitIn(node);
    case 'NOT IN'        : return this.visitNotIn(node);
    case 'CASE'          : return this.visitCase(node);
    case 'AT'            : return this.visitAt(node);
    case 'SLICE'         : return this.visitSlice(node);

    case 'LIMIT' :
    case 'OFFSET':
      return this.visitModifier(node);
    default:
      throw new Error("Unrecognized node type " + node.type);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitAddColumn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAddColumn (addColumn)](#apidoc.element.sql.dialect.prototype.visitAddColumn)
- description and source-code
```javascript
visitAddColumn = function (addColumn) {
  this._visitingAddColumn = true;
  var result = ['ADD COLUMN ' + this.visit(addColumn.nodes[0])];
  this._visitingAddColumn = false;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitAlias"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAlias (alias)](#apidoc.element.sql.dialect.prototype.visitAlias)
- description and source-code
```javascript
visitAlias = function (alias) {
  var result = [this.visit(alias.value) + this._aliasText + this.quote(alias.alias)];
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitAlter"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAlter (alter)](#apidoc.element.sql.dialect.prototype.visitAlter)
- description and source-code
```javascript
visitAlter = function (alter) {
  this._visitingAlter = true;
  // don't auto-generate from clause
  var table = this._queryNode.table;
  var result = [
    'ALTER TABLE',
    this.visit(table.toNode()),
    alter.nodes.map(this.visit.bind(this)).join(', ')
  ];
  this._visitingAlter = false;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitArrayCall"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitArrayCall (arrayCall)](#apidoc.element.sql.dialect.prototype.visitArrayCall)
- description and source-code
```javascript
visitArrayCall = function (arrayCall) {
  var txt = 'ARRAY[' + arrayCall.nodes.map(this.visit.bind(this)).join(', ') + ']';
  return [txt];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitAt"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitAt (at)](#apidoc.element.sql.dialect.prototype.visitAt)
- description and source-code
```javascript
visitAt = function (at) {
  var text = '(' + this.visit(at.value) + ')[' + this.visit(at.index) + ']';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitBinary"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitBinary (binary)](#apidoc.element.sql.dialect.prototype.visitBinary)
- description and source-code
```javascript
visitBinary = function (binary) {
  var self = this;

  binary.left.property = binary.left.name;
  binary.right.property = binary.right.name;

  var text = '(' + this.visit(binary.left) + ' ' + binary.operator + ' ';
  if (Array.isArray(binary.right)) {
    text += '(' + binary.right.map(function (node) {
      return self.visit(node);
    }).join(', ') + ')';
  }
  else {
    text += this.visit(binary.right);
  }
  text += ')';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitCascade"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCascade ()](#apidoc.element.sql.dialect.prototype.visitCascade)
- description and source-code
```javascript
visitCascade = function () {
  return ['CASCADE'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitCase"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCase (caseExp)](#apidoc.element.sql.dialect.prototype.visitCase)
- description and source-code
```javascript
visitCase = function (caseExp) {
  assert(caseExp.whenList.length == caseExp.thenList.length);

  var self = this;
  var text = '(CASE';

  this.visitingCase = true;

  for (var i = 0; i < caseExp.whenList.length; i++) {
    var whenExp = ' WHEN ' + this.visit(caseExp.whenList[i]);
    var thenExp = ' THEN ' + this.visit(caseExp.thenList[i]);
    text += whenExp + thenExp;
  }

  if (null !== caseExp.else && undefined !== caseExp.else) {
    text += ' ELSE ' + this.visit(caseExp.else);
  }

  this.visitingCase = false;

  text += ' END)';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitCast"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCast (cast)](#apidoc.element.sql.dialect.prototype.visitCast)
- description and source-code
```javascript
visitCast = function (cast) {
  this._visitingCast = true;
  var result = ['CAST(' + this.visit(cast.value) + ' AS ' + cast.dataType + ')'];
  this._visitingCast = false;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitColumn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitColumn (columnNode)](#apidoc.element.sql.dialect.prototype.visitColumn)
- description and source-code
```javascript
visitColumn = function (columnNode) {
  var table = columnNode.table;
  var inInsertUpdateClause = this._visitedInsert || this._visitingUpdateTargetColumn;
  var inDdlClause = this._visitingAddColumn || this._visitingAlter || this._visitingCreate;
  var inSelectClause =
    this.visitingReturning ||
      (!this._selectOrDeleteEndIndex
        && !this._visitingWhere   // jshint ignore:line
        && !inInsertUpdateClause  // jshint ignore:line
        && !inDdlClause           // jshint ignore:line
        && !this.visitingCase     // jshint ignore:line
        && !this._visitingJoin    // jshint ignore:line
      );
  var inFunctionCall = this._visitingFunctionCall;
  var inCast = this._visitingCast;
  var txt = [];
  var closeParen = 0;
  if(inSelectClause && (table && !table.alias || !!columnNode.alias)) {
    if (columnNode.asArray) {
      closeParen++;
      txt.push(this._arrayAggFunctionName+'(');
    }

    if (!!columnNode.aggregator) {
      closeParen++;
      txt.push(columnNode.aggregator + '(');
    }

    if (columnNode.distinct === true) {
      closeParen++;
      txt.push('DISTINCT(');
    }
  }
  if(!inInsertUpdateClause && !this.visitingReturning && !this._visitingCreate && !this._visitingAlter && !columnNode.subfieldContainer
) {
    if (table) {
      if (typeof table.alias === 'string') {
        txt.push(this.quote(table.alias));
      } else {
        if (table.getSchema()) {
          txt.push(this.quote(table.getSchema()));
          txt.push('.');
        }
        txt.push(this.quote(table.getName()));
      }
      txt.push('.');
    }
  }
  if (columnNode.star) {
    var allCols = [];
    var hasAliases = false;
    if(columnNode.aggregator !== 'COUNT') {
      var tableName = txt.join('');
      for (var i = 0; i < table.columns.length; ++i) {
        var col = table.columns[i];
        var aliased = col.name !== (col.alias || col.property);
        hasAliases = hasAliases || aliased;
        allCols.push(tableName + this.quote(col.name) + (aliased ? this._aliasText + this.quote(col.alias || col.property) : ''));
      }
    }
    if(hasAliases) {
      txt = [allCols.join(', ')];
    }
    else {
      txt.push('*');
    }
  }
  else if (columnNode.isConstant) {
    // this injects directly into SELECT statement rather than creating a parameter
    //   txt.push(this._getParameterValue(columnNode.literalValue))
    // currently thinking it is better to generate a parameter
    var value = columnNode.constantValue;
    this.params.push(value);
    txt.push(this._getParameterText(this.params.length, value));
  }
  else {
    if (columnNode.subfieldContainer) {
      txt.push('(' + this.visitColumn(columnNode.subfieldContainer) + ').');
    }
    txt.push(this.quote(columnNode.name));
  }
  if(closeParen) {
    for(var j = 0; j < closeParen; j++) {
      txt.push(')');
    }
  }
  if(inSelectClause && !inFunctionCall && !inCast && (columnNode.alias || columnNode.property !== columnNode.name)) {
    txt.push(this._aliasText + this.quote(columnNode.alias || columnNode.property));
  }
  if(this._visitingCreate || this._visitingAddColumn) {
    assert(columnNode.dataType, 'dataType missing for column ' + columnNode.name +
      ' (CREATE TABLE and ADD COLUMN statements require a dataType)');
    txt.push(' ' + columnNode.dataType);

    if (this._visitingCreate) {
      if (columnNode.primaryKey && !this._visitCreateCompoundPrimaryKey) {
        // creating a column as a primary key
        txt.push(' PRIMARY KEY');
      } else if (columnNode.notNull) {
        txt.push(' NOT NULL');
      }
      if (!columnNode.primaryKey && columnNode.unique) {
        txt.push(' UNIQUE');
      }
      if (columnNode.defaultValue !== undefined) {
        txt.push(' DEFAULT ' + this._getParameterValue(columnNode.defaultValue));
      }
    }

    if (!!columnNode.references) {
      assert.equal(typeof (columnNode.references), 'object',
        'references is not a object for column ' + columnNode.name +
        ' (REFERENCES statements within CREATE TABLE and ADD COLUMN statements' +
        ' require refrences to be ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitContainedBy"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitContainedBy (containedBy)](#apidoc.element.sql.dialect.prototype.visitContainedBy)
- description and source-code
```javascript
visitContainedBy = function (containedBy) {
  var text = this.visit(containedBy.value);
  text += ' <@ ' + this.visit(containedBy.set);
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitContains"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitContains (contains)](#apidoc.element.sql.dialect.prototype.visitContains)
- description and source-code
```javascript
visitContains = function (contains) {
  var text = this.visit(contains.value);
  text += ' @> ' + this.visit(contains.set);
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitCreate"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCreate (create)](#apidoc.element.sql.dialect.prototype.visitCreate)
- description and source-code
```javascript
visitCreate = function (create) {
  this._visitingCreate = true;
  // don't auto-generate from clause
  var table = this._queryNode.table;
  var col_nodes = table.columns.map(function(col) { return col.toNode(); });
  var foreign_key_nodes = table.foreignKeys;

   var result = ['CREATE TABLE'];
  if (create.options.isTemporary) result=['CREATE TEMPORARY TABLE'];
  result = result.concat(create.nodes.map(this.visit.bind(this)));
  result.push(this.visit(table.toNode()));
  var primary_col_nodes = col_nodes.filter(function(n) {
    return n.primaryKey;
  });
  this._visitCreateCompoundPrimaryKey = primary_col_nodes.length > 1;
  var colspec = '(' + col_nodes.map(this.visit.bind(this)).join(', ');
  if (this._visitCreateCompoundPrimaryKey) {
    colspec += ', PRIMARY KEY (';
    colspec += primary_col_nodes.map(function(node) {
      return this.quote(node.name);
    }.bind(this)).join(', ');
    colspec += ')';
  }
  if(foreign_key_nodes.length > 0) {
    colspec += ', ' + foreign_key_nodes.map(this.visit.bind(this)).join(', ');
  }
  colspec += ')';
  result.push(colspec);
  this._visitCreateCompoundPrimaryKey = false;
  this._visitingCreate = false;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitCreateIndex"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCreateIndex (node)](#apidoc.element.sql.dialect.prototype.visitCreateIndex)
- description and source-code
```javascript
visitCreateIndex = function (node) {
  if (!node.options.columns || (node.options.columns.length === 0)) {
    throw new Error('No columns defined!');
  }

  var tableName = this.visit(node.table.toNode());
  var result    = [ 'CREATE' ];

  if (node.options.type) {
    result.push(node.options.type.toUpperCase());
  }

  result = result.concat([ 'INDEX', this.quote(node.indexName()) ]);

  if (node.options.algorithm) {
    result.push("USING " + node.options.algorithm.toUpperCase());
  }

  result = result.concat([
    "ON",
    tableName,
    "(" + node.options.columns.reduce(function(result, col) {
      var column = col.name ? col.name : col.value.name;
      var direction = col.direction ? ' ' + col.direction.text : '';
      var res = result.concat(this.quote(column) + direction);
      return res;
    }.bind(this), []) + ")"
  ]);

  if (node.options.parser) {
    result.push("WITH PARSER");
    result.push(node.options.parser);
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitCreateView"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitCreateView (createView)](#apidoc.element.sql.dialect.prototype.visitCreateView)
- description and source-code
```javascript
visitCreateView = function (createView) {
  var result = ['CREATE VIEW', this.quote(createView.options.viewName), 'AS'];
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDefault"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDefault (parameter)](#apidoc.element.sql.dialect.prototype.visitDefault)
- description and source-code
```javascript
visitDefault = function (parameter) {
<span class="apidocCodeCommentSpan">  /* jshint unused: false */
</span>  return ['DEFAULT'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDelete"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDelete (del)](#apidoc.element.sql.dialect.prototype.visitDelete)
- description and source-code
```javascript
visitDelete = function (del) {
  var result = ['DELETE'];
  if (del.nodes.length) {
    result.push(del.nodes.map(this.visit.bind(this)).join(', '));
  }
  this._selectOrDeleteEndIndex = result.length;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDistinct"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDistinct (truncate)](#apidoc.element.sql.dialect.prototype.visitDistinct)
- description and source-code
```javascript
visitDistinct = function (truncate) {
  // Nothing to do here since it's handled in the SELECT clause
  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDistinctOn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDistinctOn (distinctOn)](#apidoc.element.sql.dialect.prototype.visitDistinctOn)
- description and source-code
```javascript
visitDistinctOn = function (distinctOn) {
  return ['DISTINCT ON('+distinctOn.nodes.map(this.visit.bind(this)).join(', ')+')'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDrop"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDrop (drop)](#apidoc.element.sql.dialect.prototype.visitDrop)
- description and source-code
```javascript
visitDrop = function (drop) {
  // don't auto-generate from clause
  var result = ['DROP TABLE'];
  result = result.concat(drop.nodes.map(this.visit.bind(this)));
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDropColumn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDropColumn (dropColumn)](#apidoc.element.sql.dialect.prototype.visitDropColumn)
- description and source-code
```javascript
visitDropColumn = function (dropColumn) {
  return ['DROP COLUMN ' + this.visit(dropColumn.nodes[0])];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitDropIndex"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitDropIndex (node)](#apidoc.element.sql.dialect.prototype.visitDropIndex)
- description and source-code
```javascript
visitDropIndex = function (node) {
  var result = [ 'DROP INDEX' ];

  result.push(this.quote(node.table.getSchema() || "public") + "." + this.quote(node.options.indexName));

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitForShare"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitForShare ()](#apidoc.element.sql.dialect.prototype.visitForShare)
- description and source-code
```javascript
visitForShare = function () {
  return ['FOR SHARE'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitForUpdate"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitForUpdate ()](#apidoc.element.sql.dialect.prototype.visitForUpdate)
- description and source-code
```javascript
visitForUpdate = function () {
  return ['FOR UPDATE'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitForeignKey"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitForeignKey (foreignKeyNode)](#apidoc.element.sql.dialect.prototype.visitForeignKey)
- description and source-code
```javascript
visitForeignKey = function (foreignKeyNode)
{
  var txt = [];
  if(this._visitingCreate) {
    assert(foreignKeyNode.table, 'Foreign table missing for table reference');
    assert(foreignKeyNode.columns, 'Columns missing for table reference');
    if(foreignKeyNode.refColumns !== undefined) {
      assert.equal(foreignKeyNode.columns.length, foreignKeyNode.refColumns.length, 'Number of local columns and foreign columns
 differ in table reference');
    }
    if(foreignKeyNode.name !== undefined) {
      txt.push('CONSTRAINT ' + this.quote(foreignKeyNode.name) + ' ');
    }
    txt.push('FOREIGN KEY ( ');
    for(var i = 0; i < foreignKeyNode.columns.length; i++) {
      if(i>0) {
        txt.push(', ');
      }
      txt.push(this.quote(foreignKeyNode.columns[i]));
    }
    txt.push(' ) REFERENCES ');
    if(foreignKeyNode.schema !== undefined) {
      txt.push(this.quote(foreignKeyNode.schema) + '.');
    }
    txt.push(this.quote(foreignKeyNode.table));
    if(foreignKeyNode.refColumns !== undefined) {
      txt.push(' ( ');
      for(i = 0; i < foreignKeyNode.refColumns.length; i++) {
        if(i>0) {
          txt.push(', ');
        }
        txt.push(this.quote(foreignKeyNode.refColumns[i]));
      }
      txt.push(' )');
    }
    var onDelete = foreignKeyNode.onDelete;
    if(onDelete) {
      onDelete = onDelete.toUpperCase();
      if(onDelete === 'CASCADE' || onDelete === 'RESTRICT' || onDelete === 'SET NULL' || onDelete === 'SET DEFAULT' || onDelete === '
NO ACTION') {
        txt.push(' ON DELETE ' + onDelete);
      }
    }
    var onUpdate = foreignKeyNode.onUpdate;
    if(onUpdate) {
      onUpdate = onUpdate.toUpperCase();
      if(onUpdate === 'CASCADE' || onUpdate === 'RESTRICT' || onUpdate === 'SET NULL' || onUpdate === 'SET DEFAULT' || onUpdate === '
NO ACTION') {
        txt.push(' ON UPDATE ' + onUpdate);
      }
    }
    if(foreignKeyNode.constraint) {
      txt.push(' ' + foreignKeyNode.constraint.toUpperCase());
    }
  }
  return [txt.join('')];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitFrom"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitFrom (from)](#apidoc.element.sql.dialect.prototype.visitFrom)
- description and source-code
```javascript
visitFrom = function (from) {
  var result = [];
  if (from.skipFromStatement) {
    result.push(',');
  } else {
    result.push('FROM');
  }
  for(var i = 0; i < from.nodes.length; i++) {
    result = result.concat(this.visit(from.nodes[i]));
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitFunctionCall"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitFunctionCall (functionCall)](#apidoc.element.sql.dialect.prototype.visitFunctionCall)
- description and source-code
```javascript
visitFunctionCall = function (functionCall) {
  this._visitingFunctionCall = true;
  var _this = this;

  function _extract() {
    var nodes = functionCall.nodes.map(_this.visit.bind(_this));
    if (nodes.length != 1) throw new Error('Not enough parameters passed to ' + functionCall.name + ' function');
    var txt = 'EXTRACT(' + functionCall.name + ' FROM ' + (nodes[0]+'') + ')';
    return txt;
  }

  var txt = "";
  // Override date functions since postgres (and others) uses extract
  if (['YEAR', 'MONTH', 'DAY', 'HOUR'].indexOf(functionCall.name) >= 0) txt = _extract();
  // Override CURRENT_TIMESTAMP function to remove parens
  else if ('CURRENT_TIMESTAMP' == functionCall.name) txt = functionCall.name;
  else txt = functionCall.name + '(' + functionCall.nodes.map(this.visit.bind(this)).join(', ') + ')';
  this._visitingFunctionCall = false;
  return [txt];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitGroupBy"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitGroupBy (groupBy)](#apidoc.element.sql.dialect.prototype.visitGroupBy)
- description and source-code
```javascript
visitGroupBy = function (groupBy) {
  var result = ['GROUP BY', groupBy.nodes.map(this.visit.bind(this)).join(', ')];
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitHaving"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitHaving (having)](#apidoc.element.sql.dialect.prototype.visitHaving)
- description and source-code
```javascript
visitHaving = function (having) {
  var result = ['HAVING', having.nodes.map(this.visit.bind(this)).join(' AND ')];
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitIfExists"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIfExists ()](#apidoc.element.sql.dialect.prototype.visitIfExists)
- description and source-code
```javascript
visitIfExists = function () {
  return ['IF EXISTS'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitIfNotExists"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIfNotExists ()](#apidoc.element.sql.dialect.prototype.visitIfNotExists)
- description and source-code
```javascript
visitIfNotExists = function () {
  return ['IF NOT EXISTS'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitIn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIn (binary)](#apidoc.element.sql.dialect.prototype.visitIn)
- description and source-code
```javascript
visitIn = function (binary) {
  var self = this;
  var text = '(';

  if (Array.isArray(binary.right)) {
    if (binary.right.length) {
      var params  = [];
      var hasNull = false;

      binary.right.forEach(function(node) {
        if (node.type === 'PARAMETER' && node._val === null) {
          hasNull = true;
        } else {
          params.push(self.visit(node));
        }
      });

      if (params.length) {
        text += this.visit(binary.left) + ' IN (' + params.join(', ') + ')';

        if (hasNull) {
          text += ' OR ' + this.visit(binary.left) + ' IS NULL';
        }
      } else { // implicitely has null
        text += this.visit(binary.left) + ' IS NULL';
      }
    } else {
      text += '1=0';
    }
  } else {
    text += this.visit(binary.left) + ' IN ' + this.visit(binary.right);
  }

  text += ')';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitIndexes"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitIndexes (node)](#apidoc.element.sql.dialect.prototype.visitIndexes)
- description and source-code
```javascript
visitIndexes = function (node) {
<span class="apidocCodeCommentSpan">  /* jshint unused: false */
</span>  var tableName = this._queryNode.table.getName();
  var schemaName = this._queryNode.table.getSchema() || "public";

  return [
    "SELECT relname",
    "FROM pg_class",
    "WHERE oid IN (",
    "SELECT indexrelid",
    "FROM pg_index, pg_class WHERE pg_class.relname='" + tableName + "'",
    "AND pg_class.relnamespace IN (SELECT pg_namespace.oid FROM pg_namespace WHERE nspname = '" + schemaName + "')",
    "AND pg_class.oid=pg_index.indrelid)"
  ].join(' ');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitInsert"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitInsert (insert)](#apidoc.element.sql.dialect.prototype.visitInsert)
- description and source-code
```javascript
visitInsert = function (insert) {
  var self = this;
  // don't use table.column for inserts
  this._visitedInsert = true;

  var result = ['INSERT'];
  result = result.concat(insert.nodes.map(this.visit.bind(this)));
  result.push('INTO ' + this.visit(this._queryNode.table.toNode()));
  result.push('(' + insert.columns.map(this.visit.bind(this)).join(', ') + ')');

  var paramNodes = insert.getParameters();

  if (paramNodes.length > 0) {
    var paramText = paramNodes.map(function (paramSet) {
        return paramSet.map(function (param) {
          return self.visit(param);
        }).join(', ');
      }).map(function (param) {
        return '('+param+')';
      }).join(', ');

    result.push('VALUES', paramText);

    if (result.slice(2, 5).join(' ') === '() VALUES ()') {
      result.splice(2, 3, 'DEFAULT VALUES');
    }
  }

  this._visitedInsert = false;

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitInterval"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitInterval (interval)](#apidoc.element.sql.dialect.prototype.visitInterval)
- description and source-code
```javascript
visitInterval = function (interval) {
  var parameter = '';
  function _add(n, unit) {
    if(!_.isNumber(n)) return;
    if(parameter !== '') {
      parameter += ' ';
    }
    parameter += n + ' ' + unit;
  }
  _add(interval.years, 'YEAR');
  _add(interval.months, 'MONTH');
  _add(interval.days, 'DAY');
  _add(interval.hours, 'HOUR');
  _add(interval.minutes, 'MINUTE');
  _add(interval.seconds, 'SECOND');
  if(parameter === '') parameter = '0 SECOND';
  var result = "INTERVAL '" + parameter + "'";
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitJoin"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitJoin (join)](#apidoc.element.sql.dialect.prototype.visitJoin)
- description and source-code
```javascript
visitJoin = function (join) {
  var result = [];
  this._visitingJoin = true;
  result = result.concat(this.visit(join.from));
  result = result.concat(join.subType + ' JOIN');
  result = result.concat(this.visit(join.to));
  result = result.concat('ON');
  result = result.concat(this.visit(join.on));
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitLiteral"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitLiteral (node)](#apidoc.element.sql.dialect.prototype.visitLiteral)
- description and source-code
```javascript
visitLiteral = function (node) {
  var txt = [node.literal];
  if(node.alias) {
    txt.push(this._aliasText + this.quote(node.alias));
  }
  return [txt.join('')];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitModifier"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitModifier (node)](#apidoc.element.sql.dialect.prototype.visitModifier)
- description and source-code
```javascript
visitModifier = function (node) {
  return [node.type, node.count.type ? this.visit(node.count) : node.count];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitNotIn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitNotIn (binary)](#apidoc.element.sql.dialect.prototype.visitNotIn)
- description and source-code
```javascript
visitNotIn = function (binary) {
  var self = this;
  var text = '(';

  if (Array.isArray(binary.right)) {
    if (binary.right.length) {
      var params  = [];
      var hasNull = false;

      binary.right.forEach(function(node) {
        if (node.type === 'PARAMETER' && node._val === null) {
          hasNull = true;
        } else {
          params.push(self.visit(node));
        }
      });

      if (params.length && hasNull) {
        text += 'NOT (';
        text += this.visit(binary.left) + ' IN (' + params.join(', ') + ')';
        text += ' OR ' + this.visit(binary.left) + ' IS NULL';
        text += ')';
      } else if (params.length) {
        text += this.visit(binary.left) + ' NOT IN (' + params.join(', ') + ')';
      } else { // implicitely has null
        text += this.visit(binary.left) + ' IS NOT NULL';
      }
    } else {
      text += '1=1';
    }
  } else {
    text += this.visit(binary.left) + ' NOT IN ' + this.visit(binary.right);
  }

  text += ')';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitOnConflict"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOnConflict (onConflict)](#apidoc.element.sql.dialect.prototype.visitOnConflict)
- description and source-code
```javascript
visitOnConflict = function (onConflict) {
  var result = ['ON CONFLICT'];
  var columns = [];
  var updateClause = [], i, col;
  var table = this._queryNode.table;
  if(onConflict.constraint)
    result.push(['ON CONSTRAINT', this.quote(onConflict.constraint)].join(' '));
  else if(onConflict.columns) {
    for(i=0; i < onConflict.columns.length; i++) {
      columns.push(this.quote(table.getColumn(onConflict.columns[i]).name));
    }
    result.push( '(' + columns.join(', ') + ')' );
  }

  if(onConflict.update){
    updateClause.push("DO UPDATE SET");
    var update = onConflict.update;
    var setClause = [];
    for(i=0; i<update.length; i++) {
      col = this.quote(table.getColumn(update[i]).name);
      setClause.push(col + ' = EXCLUDED.' + col);
    }
    updateClause.push(setClause.join(', '));
  }
  else
    updateClause.push('DO NOTHING');

  result.push(updateClause.join(' '));
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitOnDuplicate"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOnDuplicate (onDuplicate)](#apidoc.element.sql.dialect.prototype.visitOnDuplicate)
- description and source-code
```javascript
visitOnDuplicate = function (onDuplicate) {
  throw new Error('PostgreSQL does not allow onDuplicate clause.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitOrIgnore"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOrIgnore ()](#apidoc.element.sql.dialect.prototype.visitOrIgnore)
- description and source-code
```javascript
visitOrIgnore = function () {
  throw new Error('PostgreSQL does not allow orIgnore clause.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitOrderBy"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOrderBy (orderBy)](#apidoc.element.sql.dialect.prototype.visitOrderBy)
- description and source-code
```javascript
visitOrderBy = function (orderBy) {
  var result = ['ORDER BY', orderBy.nodes.map(this.visit.bind(this)).join(', ')];
  if (this._myClass === Postgres && this.config.nullOrder) {
      result.push('NULLS ' + this.config.nullOrder.toUpperCase());
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitOrderByValue"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOrderByValue (orderByValue)](#apidoc.element.sql.dialect.prototype.visitOrderByValue)
- description and source-code
```javascript
visitOrderByValue = function (orderByValue) {
  var text = this.visit(orderByValue.value);
  if (orderByValue.direction) {
    text += ' ' + this.visit(orderByValue.direction);
  }
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitOverlap"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitOverlap (overlap)](#apidoc.element.sql.dialect.prototype.visitOverlap)
- description and source-code
```javascript
visitOverlap = function (overlap) {
  var text = this.visit(overlap.value);
  text += ' && ' + this.visit(overlap.set);
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitParameter"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitParameter (parameter)](#apidoc.element.sql.dialect.prototype.visitParameter)
- description and source-code
```javascript
visitParameter = function (parameter) {
  // save the value into the parameters array
  var value = parameter.value();
  this.params.push(value);
  return parameter.isExplicit ? [] : [this._getParameterText(this.params.length, value)];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitPostfixUnary"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitPostfixUnary (unary)](#apidoc.element.sql.dialect.prototype.visitPostfixUnary)
- description and source-code
```javascript
visitPostfixUnary = function (unary) {
  var text = '(' + this.visit(unary.left) + ' ' + unary.operator + ')';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitPrefixUnary"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitPrefixUnary (unary)](#apidoc.element.sql.dialect.prototype.visitPrefixUnary)
- description and source-code
```javascript
visitPrefixUnary = function (unary) {
  var text = '(' + unary.operator + ' ' + this.visit(unary.left) + ')';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitQuery"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitQuery (queryNode)](#apidoc.element.sql.dialect.prototype.visitQuery)
- description and source-code
```javascript
visitQuery = function (queryNode) {
  if (this._queryNode) return this.visitSubquery(queryNode,dontParenthesizeSubQuery(this._queryNode));
  this._queryNode = queryNode;
  // need to sort the top level query nodes on visitation priority
  // so select/insert/update/delete comes before from comes before where
  var missingFrom = true;
  var hasFrom     = false;
  var createView;
  var isSelect     = false;
  var actions = [];
  var targets = [];
  var filters = [];
  for(var i = 0; i < queryNode.nodes.length; i++) {
    var node = queryNode.nodes[i];
    switch(node.type) {
      case "SELECT":
        isSelect = true; // jshint ignore:line
      case "DELETE":
        actions.push(node);
        break;
      case "INDEXES":
      case "INSERT":
      case "UPDATE":
      case "CREATE":
      case "DROP":
      case "TRUNCATE":
      case "ALTER":
        actions.push(node);
        missingFrom = false;
        break;
      case "FROM":
        node.skipFromStatement = hasFrom;
        hasFrom = true;
        missingFrom = false;
        targets.push(node);
        break;
      case "CREATE VIEW":
        createView = node;
        break;
      default:
        filters.push(node);
        break;
    }
  }
  if(!actions.length) {
    // if no actions are given, guess it's a select
    actions.push(new Select().add('*'));
    isSelect = true;
  }
  if(missingFrom && queryNode.table instanceof Table) {
	  // the instanceof handles the situation where a sql.select(some expression) is used and there should be no FROM clause
    targets.push(new From().add(queryNode.table));
  }
  if (createView) {
    if (isSelect) {
      actions.unshift(createView);
    } else {
      throw new Error('Create View requires a Select.');
    }
  }
  return this.visitQueryHelper(actions,targets,filters);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitQueryHelper"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitQueryHelper (actions, targets, filters)](#apidoc.element.sql.dialect.prototype.visitQueryHelper)
- description and source-code
```javascript
visitQueryHelper = function (actions, targets, filters){
  this.handleDistinct(actions, filters);
  // lazy-man sorting
  var sortedNodes = actions.concat(targets).concat(filters);
  for(var i = 0; i < sortedNodes.length; i++) {
    var res = this.visit(sortedNodes[i]);
    this.output = this.output.concat(res);
  }
  // implicit 'from'
  return this.output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitRename"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitRename (rename)](#apidoc.element.sql.dialect.prototype.visitRename)
- description and source-code
```javascript
visitRename = function (rename) {
  return ['RENAME TO ' + this.visit(rename.nodes[0])];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitRenameColumn"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitRenameColumn (renameColumn)](#apidoc.element.sql.dialect.prototype.visitRenameColumn)
- description and source-code
```javascript
visitRenameColumn = function (renameColumn) {
  return ['RENAME COLUMN ' + this.visit(renameColumn.nodes[0]) + ' TO ' + this.visit(renameColumn.nodes[1])];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitRestrict"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitRestrict ()](#apidoc.element.sql.dialect.prototype.visitRestrict)
- description and source-code
```javascript
visitRestrict = function () {
  return ['RESTRICT'];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitReturning"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitReturning (returning)](#apidoc.element.sql.dialect.prototype.visitReturning)
- description and source-code
```javascript
visitReturning = function (returning) {
  this.visitingReturning = true;
  var r = ['RETURNING', returning.nodes.map(this.visit.bind(this)).join(', ')];
  this.visitingReturning = false;

  return r;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitSelect"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitSelect (select)](#apidoc.element.sql.dialect.prototype.visitSelect)
- description and source-code
```javascript
visitSelect = function (select) {
  var result = ['SELECT'];

  if (select.isDistinct) result.push('DISTINCT');

  var distinctOnNode = select.nodes.filter(function (node) {return node.type === 'DISTINCT ON';}).shift();
  var nonDistinctOnNodes = select.nodes.filter(function (node) {return node.type !== 'DISTINCT ON';});

  if (distinctOnNode) {
    result.push(this.visit(distinctOnNode));
  }

  result.push(nonDistinctOnNodes.map(this.visit.bind(this)).join(', '));

  this._selectOrDeleteEndIndex = this.output.length + result.length;

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitSlice"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitSlice (slice)](#apidoc.element.sql.dialect.prototype.visitSlice)
- description and source-code
```javascript
visitSlice = function (slice) {
  var text = '(' + this.visit(slice.value) + ')';
  text += '[' + this.visit(slice.start) + ':' + this.visit(slice.end) + ']';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitSubquery"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitSubquery (queryNode, dontParenthesize)](#apidoc.element.sql.dialect.prototype.visitSubquery)
- description and source-code
```javascript
visitSubquery = function (queryNode, dontParenthesize) {
  // create another query builder of the current class to build the subquery
  var subQuery = new this._myClass(this.config);

  // let the subquery modify this instance's params array
  subQuery.params = this.params;

  // pass on the disable parameter placeholder flag
  var previousFlagStatus = subQuery._disableParameterPlaceholders;
  subQuery._disableParameterPlaceholders = this._disableParameterPlaceholders;
  try {
    subQuery.visitQuery(queryNode);
  } finally {
    // restore the flag
    subQuery._disableParameterPlaceholders = previousFlagStatus;
  }

  var alias = queryNode.alias;
  if (dontParenthesize) {
  	return [subQuery.output.join(' ') + (alias ? ' ' + this.quote(alias) : '')];
  }
  return ['(' + subQuery.output.join(' ') + ')' + (alias ? ' ' + this.quote(alias) : '')];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitTable"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitTable (tableNode)](#apidoc.element.sql.dialect.prototype.visitTable)
- description and source-code
```javascript
visitTable = function (tableNode) {
  var table = tableNode.table;
  var txt="";
  if(table.getSchema()) {
    txt = this.quote(table.getSchema());
    txt += '.';
  }
  txt += this.quote(table.getName());
  if(typeof table.alias === 'string') {
    txt += this._aliasText + this.quote(table.alias);
  }
  return [txt];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitTernary"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitTernary (ternary)](#apidoc.element.sql.dialect.prototype.visitTernary)
- description and source-code
```javascript
visitTernary = function (ternary) {
  var self = this;
  var text = '(' + this.visit(ternary.left) + ' ' + ternary.operator + ' ';

  var visitPart = function(value) {
    var text = '';
    if (Array.isArray(value)) {
      text += '(' + value.map(function (node) {
        return self.visit(node);
      }).join(', ') + ')';
    }
    else {
      text += self.visit(value);
    }
    return text;
  };

  text += visitPart(ternary.middle);
  text += ' ' + ternary.separator + ' ';
  text += visitPart(ternary.right);

  text += ')';
  return [text];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitTruncate"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitTruncate (truncate)](#apidoc.element.sql.dialect.prototype.visitTruncate)
- description and source-code
```javascript
visitTruncate = function (truncate) {
  var result = ['TRUNCATE TABLE'];
  result = result.concat(truncate.nodes.map(this.visit.bind(this)));
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitUpdate"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitUpdate (update)](#apidoc.element.sql.dialect.prototype.visitUpdate)
- description and source-code
```javascript
visitUpdate = function (update) {
  // don't auto-generate from clause
  var params = [];
<span class="apidocCodeCommentSpan">  /* jshint boss: true */
</span>  for(var i = 0, node; node = update.nodes[i]; i++) {
    this._visitingUpdateTargetColumn = true;
    var target_col = this.visit(node);
    this._visitingUpdateTargetColumn = false;
    params = params.concat(target_col + ' = ' + this.visit(node.value));
  }
  var result = [
    'UPDATE',
    this.visit(this._queryNode.table.toNode()),
    'SET',
    params.join(', ')
  ];
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.dialect.prototype.visitWhere"></a>[function <span class="apidocSignatureSpan">sql.dialect.prototype.</span>visitWhere (where)](#apidoc.element.sql.dialect.prototype.visitWhere)
- description and source-code
```javascript
visitWhere = function (where) {
  this._visitingWhere = true;
  var result = ['WHERE', where.nodes.map(this.visit.bind(this)).join(', ')];
  this._visitingWhere = false;
  return result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sql.functions"></a>[module sql.functions](#apidoc.module.sql.functions)

#### <a name="apidoc.element.sql.functions.ABS"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>ABS ()](#apidoc.element.sql.functions.ABS)
- description and source-code
```javascript
ABS = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.AVG"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>AVG ()](#apidoc.element.sql.functions.AVG)
- description and source-code
```javascript
AVG = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.COALESCE"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>COALESCE ()](#apidoc.element.sql.functions.COALESCE)
- description and source-code
```javascript
COALESCE = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.COUNT"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>COUNT ()](#apidoc.element.sql.functions.COUNT)
- description and source-code
```javascript
COUNT = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.CURRENT_TIMESTAMP"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>CURRENT_TIMESTAMP ()](#apidoc.element.sql.functions.CURRENT_TIMESTAMP)
- description and source-code
```javascript
CURRENT_TIMESTAMP = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.DAY"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>DAY ()](#apidoc.element.sql.functions.DAY)
- description and source-code
```javascript
DAY = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.DISTINCT"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>DISTINCT ()](#apidoc.element.sql.functions.DISTINCT)
- description and source-code
```javascript
DISTINCT = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.HOUR"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>HOUR ()](#apidoc.element.sql.functions.HOUR)
- description and source-code
```javascript
HOUR = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.HSTORE"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>HSTORE ()](#apidoc.element.sql.functions.HSTORE)
- description and source-code
```javascript
HSTORE = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.LEFT"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>LEFT ()](#apidoc.element.sql.functions.LEFT)
- description and source-code
```javascript
LEFT = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.LENGTH"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>LENGTH ()](#apidoc.element.sql.functions.LENGTH)
- description and source-code
```javascript
LENGTH = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.LOWER"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>LOWER ()](#apidoc.element.sql.functions.LOWER)
- description and source-code
```javascript
LOWER = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.LTRIM"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>LTRIM ()](#apidoc.element.sql.functions.LTRIM)
- description and source-code
```javascript
LTRIM = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.MAX"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>MAX ()](#apidoc.element.sql.functions.MAX)
- description and source-code
```javascript
MAX = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.MIN"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>MIN ()](#apidoc.element.sql.functions.MIN)
- description and source-code
```javascript
MIN = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.MONTH"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>MONTH ()](#apidoc.element.sql.functions.MONTH)
- description and source-code
```javascript
MONTH = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.PLAINTO_TSQUERY"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>PLAINTO_TSQUERY ()](#apidoc.element.sql.functions.PLAINTO_TSQUERY)
- description and source-code
```javascript
PLAINTO_TSQUERY = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.RANDOM"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>RANDOM ()](#apidoc.element.sql.functions.RANDOM)
- description and source-code
```javascript
RANDOM = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.RIGHT"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>RIGHT ()](#apidoc.element.sql.functions.RIGHT)
- description and source-code
```javascript
RIGHT = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.ROUND"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>ROUND ()](#apidoc.element.sql.functions.ROUND)
- description and source-code
```javascript
ROUND = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.RTRIM"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>RTRIM ()](#apidoc.element.sql.functions.RTRIM)
- description and source-code
```javascript
RTRIM = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.SETWEIGHT"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>SETWEIGHT ()](#apidoc.element.sql.functions.SETWEIGHT)
- description and source-code
```javascript
SETWEIGHT = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.SUBSTR"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>SUBSTR ()](#apidoc.element.sql.functions.SUBSTR)
- description and source-code
```javascript
SUBSTR = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.SUM"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>SUM ()](#apidoc.element.sql.functions.SUM)
- description and source-code
```javascript
SUM = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.TO_TSQUERY"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>TO_TSQUERY ()](#apidoc.element.sql.functions.TO_TSQUERY)
- description and source-code
```javascript
TO_TSQUERY = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.TO_TSVECTOR"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>TO_TSVECTOR ()](#apidoc.element.sql.functions.TO_TSVECTOR)
- description and source-code
```javascript
TO_TSVECTOR = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.TRIM"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>TRIM ()](#apidoc.element.sql.functions.TRIM)
- description and source-code
```javascript
TRIM = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.TS_RANK"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>TS_RANK ()](#apidoc.element.sql.functions.TS_RANK)
- description and source-code
```javascript
TS_RANK = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.TS_RANK_CD"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>TS_RANK_CD ()](#apidoc.element.sql.functions.TS_RANK_CD)
- description and source-code
```javascript
TS_RANK_CD = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.UPPER"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>UPPER ()](#apidoc.element.sql.functions.UPPER)
- description and source-code
```javascript
UPPER = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sql.functions.YEAR"></a>[function <span class="apidocSignatureSpan">sql.functions.</span>YEAR ()](#apidoc.element.sql.functions.YEAR)
- description and source-code
```javascript
YEAR = function () {
  // turn array-like arguments object into a true array
  return new FunctionCall(name, sliced(arguments));
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
