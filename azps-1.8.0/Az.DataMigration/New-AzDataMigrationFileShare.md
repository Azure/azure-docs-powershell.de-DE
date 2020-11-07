---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: cc09f7ac0a5f4378c65700cd9681118200d629ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820116"
---
# <span data-ttu-id="acd37-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="acd37-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="acd37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="acd37-102">SYNOPSIS</span></span>
<span data-ttu-id="acd37-103">Erstellt das FileShare-Objekt für den Azure-Daten Bank Migrationsdienst, der die lokale Netzwerkfreigabe angibt, auf die die Quelldaten Bank Sicherungen übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="acd37-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="acd37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="acd37-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acd37-105">DESCRIPTION</span></span>
<span data-ttu-id="acd37-106">Das New-AzDataMigrationFileShare-Cmdlet erstellt das FileShare-Objekt, das die lokale Netzwerkfreigabe angibt, auf die der Azure-Daten Bank Migrationsdienst Quelldaten Bank Sicherungen durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="acd37-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="acd37-107">Das Dienstkonto, auf dem die Quell-SQL Server-Instanz ausgeführt wird, muss über Schreibberechtigungen für diese Netzwerkfreigabe verfügen.</span><span class="sxs-lookup"><span data-stu-id="acd37-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="acd37-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="acd37-108">EXAMPLES</span></span>

### <span data-ttu-id="acd37-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="acd37-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="acd37-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="acd37-110">PARAMETERS</span></span>

### <span data-ttu-id="acd37-111">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="acd37-111">-Credential</span></span>
<span data-ttu-id="acd37-112">Anmeldeinformationen für den Zugriff auf die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="acd37-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="acd37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd37-113">-DefaultProfile</span></span>
<span data-ttu-id="acd37-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="acd37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd37-115">-Path</span><span class="sxs-lookup"><span data-stu-id="acd37-115">-Path</span></span>
<span data-ttu-id="acd37-116">Dateifreigabepfad.</span><span class="sxs-lookup"><span data-stu-id="acd37-116">File share path.</span></span>

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

### <span data-ttu-id="acd37-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd37-117">CommonParameters</span></span>
<span data-ttu-id="acd37-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd37-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd37-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acd37-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd37-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="acd37-120">INPUTS</span></span>

### <span data-ttu-id="acd37-121">Keine</span><span class="sxs-lookup"><span data-stu-id="acd37-121">None</span></span>

## <span data-ttu-id="acd37-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="acd37-122">OUTPUTS</span></span>

### <span data-ttu-id="acd37-123">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="acd37-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="acd37-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="acd37-124">NOTES</span></span>

## <span data-ttu-id="acd37-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="acd37-125">RELATED LINKS</span></span>
