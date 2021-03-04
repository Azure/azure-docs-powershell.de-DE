---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: b30f9fd4b29a1be064a9e0925e39faa71485b58f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925904"
---
# <span data-ttu-id="37ed0-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="37ed0-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="37ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="37ed0-103">Erstellt das FileShare-Objekt für den Azure Database Migration Service, der die lokale Netzwerkfreigabe angibt, in die die Quelldatenbanksicherungen ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37ed0-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="37ed0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37ed0-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37ed0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="37ed0-106">Das New-AzDataMigrationFileShare-Cmdlet erstellt das FileShare-Objekt, das die lokale Netzwerkfreigabe angibt, in die der Azure Database Migration Service Quelldatenbanksicherungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="37ed0-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="37ed0-107">Das Dienstkonto, auf dem SQL Server Instanz ausgeführt wird, muss über Schreibberechtigungen für diese Netzwerkfreigabe verfügen.</span><span class="sxs-lookup"><span data-stu-id="37ed0-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="37ed0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37ed0-108">EXAMPLES</span></span>

### <span data-ttu-id="37ed0-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37ed0-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="37ed0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="37ed0-110">PARAMETERS</span></span>

### <span data-ttu-id="37ed0-111">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="37ed0-111">-Credential</span></span>
<span data-ttu-id="37ed0-112">Anmeldeinformationen für den Zugriff auf die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="37ed0-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ed0-113">-DefaultProfile</span></span>
<span data-ttu-id="37ed0-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37ed0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ed0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="37ed0-115">-Path</span></span>
<span data-ttu-id="37ed0-116">Dateifreigabepfad.</span><span class="sxs-lookup"><span data-stu-id="37ed0-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ed0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ed0-117">CommonParameters</span></span>
<span data-ttu-id="37ed0-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ed0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ed0-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ed0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ed0-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37ed0-120">INPUTS</span></span>

### <span data-ttu-id="37ed0-121">Keine</span><span class="sxs-lookup"><span data-stu-id="37ed0-121">None</span></span>

## <span data-ttu-id="37ed0-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37ed0-122">OUTPUTS</span></span>

### <span data-ttu-id="37ed0-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="37ed0-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="37ed0-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="37ed0-124">NOTES</span></span>

## <span data-ttu-id="37ed0-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="37ed0-125">RELATED LINKS</span></span>
