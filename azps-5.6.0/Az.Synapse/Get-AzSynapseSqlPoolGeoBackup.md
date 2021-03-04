---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921547"
---
# <span data-ttu-id="b5bd3-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b5bd3-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="b5bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bd3-103">Ruft eine georedundant gesicherte Sicherung eines Sql-Pools ab.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="b5bd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5bd3-104">SYNTAX</span></span>

### <span data-ttu-id="b5bd3-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5bd3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5bd3-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="b5bd3-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5bd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="b5bd3-108">Das **Get-AzSynapseSqlPoolGeoBackup-Cmdlet** ruft eine angegebene georedundierte Sicherung eines SQL-Pools oder alle verfügbaren georedundierten Sicherungen in einem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="b5bd3-109">Eine georedundant gesicherte Ressource ist eine restorable Ressource, die Datendateien von einem separaten geografischen Speicherort verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="b5bd3-110">Sie können Geo-Restore verwenden, um eine georedundant gesicherte Sicherung im Fall eines regionalen Ausfalls wiederherzustellen, um Ihren Sql Pool in einer neuen Region wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="b5bd3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5bd3-111">EXAMPLES</span></span>

### <span data-ttu-id="b5bd3-112">Beispiel 1: Erhalten einer angegebenen geo redundanten Sicherung</span><span class="sxs-lookup"><span data-stu-id="b5bd3-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="b5bd3-113">Das Cmdlet ruft Die Geosicherung für einen SQL-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="b5bd3-114">Beispiel 2: Erhalten aller georedundanter Sicherungen in einem Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="b5bd3-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="b5bd3-115">Mit diesem Befehl werden alle verfügbaren georedundanziellen Sicherungen in einem angegebenen Arbeitsbereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="b5bd3-116">Beispiel 3: Erhalten aller georedundanter Sicherungen in einem Arbeitsbereich mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="b5bd3-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="b5bd3-117">Mit diesem Befehl werden alle verfügbaren georedundanziellen Sicherungen für einen angegebenen Arbeitsbereich, der mit "Contoso" beginnt, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="b5bd3-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5bd3-118">PARAMETERS</span></span>

### <span data-ttu-id="b5bd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bd3-119">-DefaultProfile</span></span>
<span data-ttu-id="b5bd3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5bd3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b5bd3-121">-Name</span></span>
<span data-ttu-id="b5bd3-122">Der Synapse Sql-Pool.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bd3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5bd3-123">-ResourceId</span></span>
<span data-ttu-id="b5bd3-124">Geben Sie eine Sql Pool Geo Backup Resource ID ein.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5bd3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5bd3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5bd3-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bd3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5bd3-127">-WorkspaceName</span></span>
<span data-ttu-id="b5bd3-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bd3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bd3-129">CommonParameters</span></span>
<span data-ttu-id="b5bd3-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bd3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bd3-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5bd3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bd3-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5bd3-132">INPUTS</span></span>

### <span data-ttu-id="b5bd3-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5bd3-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b5bd3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5bd3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="b5bd3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5bd3-135">OUTPUTS</span></span>

### <span data-ttu-id="b5bd3-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="b5bd3-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="b5bd3-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5bd3-137">NOTES</span></span>

## <span data-ttu-id="b5bd3-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5bd3-138">RELATED LINKS</span></span>
