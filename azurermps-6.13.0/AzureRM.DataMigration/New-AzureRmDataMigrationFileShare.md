---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502114"
---
# <span data-ttu-id="3a112-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="3a112-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="3a112-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a112-102">SYNOPSIS</span></span>
<span data-ttu-id="3a112-103">Erstellt das FileShare-Objekt für den Azure-Daten Bank Migrationsdienst, der die lokale Netzwerkfreigabe angibt, auf die die Quelldaten Bank Sicherungen übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a112-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a112-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a112-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a112-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a112-105">DESCRIPTION</span></span>
<span data-ttu-id="3a112-106">Das New-AzureRmDataMigrationFileShare-Cmdlet erstellt das FileShare-Objekt, das die lokale Netzwerkfreigabe angibt, auf die der Azure-Daten Bank Migrationsdienst Quelldaten Bank Sicherungen durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="3a112-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="3a112-107">Das Dienstkonto, auf dem die Quell-SQL Server-Instanz ausgeführt wird, muss über Schreibberechtigungen für diese Netzwerkfreigabe verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a112-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="3a112-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a112-108">EXAMPLES</span></span>

### <span data-ttu-id="3a112-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a112-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="3a112-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a112-110">PARAMETERS</span></span>

### <span data-ttu-id="3a112-111">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="3a112-111">-Credential</span></span>
<span data-ttu-id="3a112-112">Anmeldeinformationen für den Zugriff auf die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="3a112-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="3a112-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a112-113">-DefaultProfile</span></span>
<span data-ttu-id="3a112-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a112-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a112-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3a112-115">-Path</span></span>
<span data-ttu-id="3a112-116">Dateifreigabepfad.</span><span class="sxs-lookup"><span data-stu-id="3a112-116">File share path.</span></span>

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

### <span data-ttu-id="3a112-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a112-117">CommonParameters</span></span>
<span data-ttu-id="3a112-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a112-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a112-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a112-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a112-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a112-120">INPUTS</span></span>

### <span data-ttu-id="3a112-121">Keine</span><span class="sxs-lookup"><span data-stu-id="3a112-121">None</span></span>

## <span data-ttu-id="3a112-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a112-122">OUTPUTS</span></span>

### <span data-ttu-id="3a112-123">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="3a112-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="3a112-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a112-124">NOTES</span></span>

## <span data-ttu-id="3a112-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a112-125">RELATED LINKS</span></span>
