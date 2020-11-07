---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2e5e313fe35770e6841909e1f0718cfe3d9c8664
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663416"
---
# <span data-ttu-id="80556-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="80556-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="80556-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80556-102">SYNOPSIS</span></span>
<span data-ttu-id="80556-103">Ruft eine Daten Bank Geo-Sicherungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="80556-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80556-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80556-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80556-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80556-105">DESCRIPTION</span></span>
<span data-ttu-id="80556-106">Das Cmdlet " **Get-AzureRmSqlDatabaseGeoBackupPolicy** " Ruft die für diese Datenbank registrierte Geo-Sicherungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="80556-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="80556-107">Hierbei handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80556-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="80556-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80556-108">EXAMPLES</span></span>

## <span data-ttu-id="80556-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="80556-109">PARAMETERS</span></span>

### <span data-ttu-id="80556-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80556-110">-DatabaseName</span></span>
<span data-ttu-id="80556-111">Gibt den Namen der Datenbank an, für die dieses Cmdlet die Geo-Sicherungsrichtlinie erhält.</span><span class="sxs-lookup"><span data-stu-id="80556-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80556-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80556-112">-DefaultProfile</span></span>
<span data-ttu-id="80556-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80556-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80556-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80556-114">-ResourceGroupName</span></span>
<span data-ttu-id="80556-115">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="80556-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80556-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="80556-116">-ServerName</span></span>
<span data-ttu-id="80556-117">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="80556-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80556-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80556-118">CommonParameters</span></span>
<span data-ttu-id="80556-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80556-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80556-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80556-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80556-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80556-121">INPUTS</span></span>

### <span data-ttu-id="80556-122">Keine</span><span class="sxs-lookup"><span data-stu-id="80556-122">None</span></span>
<span data-ttu-id="80556-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="80556-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80556-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80556-124">OUTPUTS</span></span>

## <span data-ttu-id="80556-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="80556-125">NOTES</span></span>

## <span data-ttu-id="80556-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80556-126">RELATED LINKS</span></span>

[<span data-ttu-id="80556-127">Satz-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="80556-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="80556-128">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="80556-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
