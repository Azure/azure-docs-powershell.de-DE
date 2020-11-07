---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663158"
---
# <span data-ttu-id="d802d-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d802d-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="d802d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d802d-102">SYNOPSIS</span></span>
<span data-ttu-id="d802d-103">Erstellt ein neues Verbindungs Info Objekt, das den Servertyp und den Namen für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="d802d-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d802d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d802d-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d802d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d802d-105">DESCRIPTION</span></span>
<span data-ttu-id="d802d-106">Das New-AzureRmDataMigrationConnectionInfo-Cmdlet erstellt ein neues Verbindungs Info Objekt, das den Servertyp für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="d802d-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="d802d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d802d-107">EXAMPLES</span></span>

### <span data-ttu-id="d802d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d802d-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="d802d-109">Im vorangehenden Beispiel wird ein neues verbindungsinformationsobjekt erstellt, das SQL als ServerType-Parameter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d802d-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="d802d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d802d-110">PARAMETERS</span></span>

### <span data-ttu-id="d802d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d802d-111">-DefaultProfile</span></span>
<span data-ttu-id="d802d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d802d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d802d-113">-Servertyp</span><span class="sxs-lookup"><span data-stu-id="d802d-113">-ServerType</span></span>
<span data-ttu-id="d802d-114">Enum, die den Servertyp beschreibt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d802d-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="d802d-115">Derzeit unterstützte Werte sind SQL für SQL Server, Azure SQL Managed-Instanz und Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d802d-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d802d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d802d-116">CommonParameters</span></span>
<span data-ttu-id="d802d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d802d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d802d-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d802d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d802d-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d802d-119">INPUTS</span></span>

### <span data-ttu-id="d802d-120">Keine</span><span class="sxs-lookup"><span data-stu-id="d802d-120">None</span></span>

## <span data-ttu-id="d802d-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d802d-121">OUTPUTS</span></span>

### <span data-ttu-id="d802d-122">Microsoft. Azure. Management. datamigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d802d-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="d802d-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d802d-123">NOTES</span></span>

## <span data-ttu-id="d802d-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d802d-124">RELATED LINKS</span></span>
