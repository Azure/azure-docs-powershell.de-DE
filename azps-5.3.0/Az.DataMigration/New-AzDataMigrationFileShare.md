---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387580"
---
# <span data-ttu-id="03c60-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="03c60-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="03c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c60-102">SYNOPSIS</span></span>
<span data-ttu-id="03c60-103">Erstellt das Objekt "FileShare" für den Azure-Datenbankmigrationsdienst, der die lokale Netzwerkfreigabe angibt, an die die Quelldatenbanksicherungen durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="03c60-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="03c60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03c60-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03c60-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03c60-105">DESCRIPTION</span></span>
<span data-ttu-id="03c60-106">Das New-AzDataMigrationFileShare erstellt das FileShare-Objekt, das die lokale Netzwerkfreigabe angibt, auf die der Azure Database Migration Service Quelldatenbanksicherungen erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="03c60-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="03c60-107">Das Dienstkonto, auf dem die SQL Server ausgeführt wird, muss über Schreibberechtigungen für diese Netzwerkfreigabe verfügen.</span><span class="sxs-lookup"><span data-stu-id="03c60-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="03c60-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03c60-108">EXAMPLES</span></span>

### <span data-ttu-id="03c60-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03c60-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="03c60-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c60-110">PARAMETERS</span></span>

### <span data-ttu-id="03c60-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="03c60-111">-Credential</span></span>
<span data-ttu-id="03c60-112">Anmeldeinformationen für den Zugriff auf die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="03c60-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="03c60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c60-113">-DefaultProfile</span></span>
<span data-ttu-id="03c60-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03c60-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c60-115">-Path</span><span class="sxs-lookup"><span data-stu-id="03c60-115">-Path</span></span>
<span data-ttu-id="03c60-116">Dateifreigabepfad.</span><span class="sxs-lookup"><span data-stu-id="03c60-116">File share path.</span></span>

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

### <span data-ttu-id="03c60-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c60-117">CommonParameters</span></span>
<span data-ttu-id="03c60-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c60-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c60-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c60-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c60-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03c60-120">INPUTS</span></span>

### <span data-ttu-id="03c60-121">Keine</span><span class="sxs-lookup"><span data-stu-id="03c60-121">None</span></span>

## <span data-ttu-id="03c60-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03c60-122">OUTPUTS</span></span>

### <span data-ttu-id="03c60-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="03c60-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="03c60-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03c60-124">NOTES</span></span>

## <span data-ttu-id="03c60-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03c60-125">RELATED LINKS</span></span>
