---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297663"
---
# <span data-ttu-id="e7ab0-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e7ab0-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="e7ab0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ab0-103">Erstellt ein neues Verbindungs Info Objekt, das den Servertyp und den Namen für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="e7ab0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7ab0-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7ab0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ab0-106">Das New-AzDataMigrationConnectionInfo-Cmdlet erstellt ein neues Verbindungs Info Objekt, das den Servertyp für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="e7ab0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7ab0-107">EXAMPLES</span></span>

### <span data-ttu-id="e7ab0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7ab0-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="e7ab0-109">Im vorangehenden Beispiel wird ein neues verbindungsinformationsobjekt erstellt, das SQL als ServerType-Parameter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="e7ab0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7ab0-110">PARAMETERS</span></span>

### <span data-ttu-id="e7ab0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ab0-111">-DefaultProfile</span></span>
<span data-ttu-id="e7ab0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ab0-113">-Servertyp</span><span class="sxs-lookup"><span data-stu-id="e7ab0-113">-ServerType</span></span>
<span data-ttu-id="e7ab0-114">Enum, die den Servertyp beschreibt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="e7ab0-115">Derzeit unterstützte Werte sind SQL für SQL Server, Azure SQL Managed instance, MongoDB, CosmosDb und Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ab0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ab0-116">CommonParameters</span></span>
<span data-ttu-id="e7ab0-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ab0-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ab0-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ab0-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7ab0-119">INPUTS</span></span>

### <span data-ttu-id="e7ab0-120">Keine</span><span class="sxs-lookup"><span data-stu-id="e7ab0-120">None</span></span>

## <span data-ttu-id="e7ab0-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7ab0-121">OUTPUTS</span></span>

### <span data-ttu-id="e7ab0-122">Microsoft. Azure. Management. datamigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e7ab0-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="e7ab0-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7ab0-123">NOTES</span></span>

## <span data-ttu-id="e7ab0-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7ab0-124">RELATED LINKS</span></span>
