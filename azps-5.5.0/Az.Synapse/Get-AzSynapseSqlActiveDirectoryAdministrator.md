---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164604"
---
# <span data-ttu-id="ba027-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ba027-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ba027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba027-102">SYNOPSIS</span></span>
<span data-ttu-id="ba027-103">Ruft Informationen zu einem Azure AD-Administrator für Synapse Analytics Workspace ab.</span><span class="sxs-lookup"><span data-stu-id="ba027-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="ba027-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba027-104">SYNTAX</span></span>

### <span data-ttu-id="ba027-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba027-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba027-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba027-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba027-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba027-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba027-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba027-108">DESCRIPTION</span></span>
<span data-ttu-id="ba027-109">Das **Cmdlet "Get-AzSynapseSqlActiveDirectoryAdministrator"** ruft Informationen über einen Azure Active Directory (Azure AD)-Administrator für einen Azure Synapse Analytics Workspace im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ba027-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="ba027-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba027-110">EXAMPLES</span></span>

### <span data-ttu-id="ba027-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba027-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ba027-112">Dieser Befehl ruft Informationen über einen Azure AD-Administrator für einen Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="ba027-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ba027-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba027-113">PARAMETERS</span></span>

### <span data-ttu-id="ba027-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba027-114">-DefaultProfile</span></span>
<span data-ttu-id="ba027-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba027-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba027-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba027-116">-InputObject</span></span>
<span data-ttu-id="ba027-117">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba027-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba027-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba027-118">-ResourceGroupName</span></span>
<span data-ttu-id="ba027-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ba027-119">Resource group name.</span></span>

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

### <span data-ttu-id="ba027-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba027-120">-ResourceId</span></span>
<span data-ttu-id="ba027-121">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ba027-121">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba027-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba027-122">-WorkspaceName</span></span>
<span data-ttu-id="ba027-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ba027-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ba027-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba027-124">CommonParameters</span></span>
<span data-ttu-id="ba027-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba027-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba027-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba027-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba027-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba027-127">INPUTS</span></span>

### <span data-ttu-id="ba027-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba027-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ba027-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba027-129">OUTPUTS</span></span>

### <span data-ttu-id="ba027-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="ba027-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="ba027-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ba027-131">NOTES</span></span>

## <span data-ttu-id="ba027-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ba027-132">RELATED LINKS</span></span>
