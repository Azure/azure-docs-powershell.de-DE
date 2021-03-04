---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: cfd8df9bc329ef252c28ef826b1ba68a1946bab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925931"
---
# <span data-ttu-id="e7db6-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e7db6-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="e7db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7db6-102">SYNOPSIS</span></span>
<span data-ttu-id="e7db6-103">Erstellt ein neues Verbindungsinfoobjekt, das den Servertyp und den Namen für die Verbindung an gibt.</span><span class="sxs-lookup"><span data-stu-id="e7db6-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="e7db6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7db6-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7db6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7db6-105">DESCRIPTION</span></span>
<span data-ttu-id="e7db6-106">Das New-AzDataMigrationConnectionInfo-Cmdlet erstellt ein neues Verbindungsinfoobjekt, das den Servertyp für die Verbindung an gibt.</span><span class="sxs-lookup"><span data-stu-id="e7db6-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="e7db6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7db6-107">EXAMPLES</span></span>

### <span data-ttu-id="e7db6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7db6-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="e7db6-109">Im vorherigen Beispiel wird ein neues Verbindungsinfoobjekt erstellt, das SQL ServerType-Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="e7db6-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="e7db6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7db6-110">PARAMETERS</span></span>

### <span data-ttu-id="e7db6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7db6-111">-DefaultProfile</span></span>
<span data-ttu-id="e7db6-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7db6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7db6-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="e7db6-113">-ServerType</span></span>
<span data-ttu-id="e7db6-114">Enumeration, die den Servertyp beschreibt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7db6-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="e7db6-115">Aktuell unterstützte Werte werden SQL für SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb und Azure SQL Database verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7db6-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="e7db6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7db6-116">CommonParameters</span></span>
<span data-ttu-id="e7db6-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7db6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7db6-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7db6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7db6-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7db6-119">INPUTS</span></span>

### <span data-ttu-id="e7db6-120">Keine</span><span class="sxs-lookup"><span data-stu-id="e7db6-120">None</span></span>

## <span data-ttu-id="e7db6-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7db6-121">OUTPUTS</span></span>

### <span data-ttu-id="e7db6-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e7db6-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="e7db6-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e7db6-123">NOTES</span></span>

## <span data-ttu-id="e7db6-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e7db6-124">RELATED LINKS</span></span>
