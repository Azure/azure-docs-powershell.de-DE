---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300835"
---
# <span data-ttu-id="86274-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86274-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="86274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86274-102">SYNOPSIS</span></span>
<span data-ttu-id="86274-103">Ruft eine Assembly für das Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="86274-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="86274-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86274-104">SYNTAX</span></span>

### <span data-ttu-id="86274-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="86274-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86274-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="86274-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86274-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86274-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86274-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86274-108">DESCRIPTION</span></span>
<span data-ttu-id="86274-109">Das **Cmdlet "Get-AzIntegrationAccountAssembly"** ruft eine Assembly aus einem Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="86274-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="86274-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86274-110">EXAMPLES</span></span>

### <span data-ttu-id="86274-111">Beispiel 1: Erhalten einer Assembly nach Parametern</span><span class="sxs-lookup"><span data-stu-id="86274-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="86274-112">Sie erhalten eine Assembly namens "sampleAssembly" im Integrationskonto "sampleIntegrationAccount", das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="86274-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="86274-113">Beispiel 2: Auflisten aller Assemblys in einem Integrationskonto nach Parametern</span><span class="sxs-lookup"><span data-stu-id="86274-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="86274-114">Holen Sie sich alle Assemblys im Integrationskonto "sampleIntegrationAccount", das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="86274-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="86274-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86274-115">PARAMETERS</span></span>

### <span data-ttu-id="86274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86274-116">-DefaultProfile</span></span>
<span data-ttu-id="86274-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86274-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86274-118">-Name</span><span class="sxs-lookup"><span data-stu-id="86274-118">-Name</span></span>
<span data-ttu-id="86274-119">Der Name der Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="86274-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86274-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="86274-120">-ParentName</span></span>
<span data-ttu-id="86274-121">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="86274-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86274-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="86274-122">-ParentObject</span></span>
<span data-ttu-id="86274-123">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="86274-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86274-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="86274-124">-ParentResourceId</span></span>
<span data-ttu-id="86274-125">Die Ressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="86274-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86274-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86274-126">-ResourceGroupName</span></span>
<span data-ttu-id="86274-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="86274-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86274-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86274-128">CommonParameters</span></span>
<span data-ttu-id="86274-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86274-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86274-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86274-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86274-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86274-131">INPUTS</span></span>

### <span data-ttu-id="86274-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="86274-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="86274-133">System.String</span><span class="sxs-lookup"><span data-stu-id="86274-133">System.String</span></span>

## <span data-ttu-id="86274-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86274-134">OUTPUTS</span></span>

### <span data-ttu-id="86274-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86274-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="86274-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="86274-136">NOTES</span></span>

## <span data-ttu-id="86274-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="86274-137">RELATED LINKS</span></span>
