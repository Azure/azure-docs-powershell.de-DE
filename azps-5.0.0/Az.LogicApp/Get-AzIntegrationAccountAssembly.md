---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178865"
---
# <span data-ttu-id="8e7d7-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8e7d7-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="8e7d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7d7-103">Ruft eine Integration Account-Assembly ab.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="8e7d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e7d7-104">SYNTAX</span></span>

### <span data-ttu-id="8e7d7-105">ByIntegrationAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e7d7-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e7d7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e7d7-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e7d7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7d7-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e7d7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e7d7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e7d7-109">Das Cmdlet " **Get-AzIntegrationAccountAssembly** " Ruft eine Assembly von einem Integrations Konto ab.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="8e7d7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e7d7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e7d7-111">Beispiel 1: Abrufen einer Assembly anhand von Parametern</span><span class="sxs-lookup"><span data-stu-id="8e7d7-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="8e7d7-112">Rufen Sie eine Assembly mit dem Namen "SampleAssembly" ab, die sich im Integrations Konto "sampleIntegrationAccount" befindet, das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="8e7d7-113">Beispiel 2: Auflisten aller Assemblys in einem Integrations Konto nach Parametern</span><span class="sxs-lookup"><span data-stu-id="8e7d7-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="8e7d7-114">Rufen Sie alle Assemblys ab, die sich im Integrations Konto "sampleIntegrationAccount" befinden, das in der Ressourcengruppe "sampleResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="8e7d7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e7d7-115">PARAMETERS</span></span>

### <span data-ttu-id="8e7d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7d7-116">-DefaultProfile</span></span>
<span data-ttu-id="8e7d7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e7d7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8e7d7-118">-Name</span></span>
<span data-ttu-id="8e7d7-119">Der Name der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="8e7d7-120">-Übergeordneter</span><span class="sxs-lookup"><span data-stu-id="8e7d7-120">-ParentName</span></span>
<span data-ttu-id="8e7d7-121">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-121">The integration account name.</span></span>

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

### <span data-ttu-id="8e7d7-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e7d7-122">-ParentObject</span></span>
<span data-ttu-id="8e7d7-123">Ein Integrations Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-123">An integration account object.</span></span>

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

### <span data-ttu-id="8e7d7-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7d7-124">-ParentResourceId</span></span>
<span data-ttu-id="8e7d7-125">Die Ressourcen-ID des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="8e7d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e7d7-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-127">The resource group name.</span></span>

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

### <span data-ttu-id="8e7d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7d7-128">CommonParameters</span></span>
<span data-ttu-id="8e7d7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7d7-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7d7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7d7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e7d7-131">INPUTS</span></span>

### <span data-ttu-id="8e7d7-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8e7d7-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="8e7d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7d7-133">System.String</span></span>

## <span data-ttu-id="8e7d7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e7d7-134">OUTPUTS</span></span>

### <span data-ttu-id="8e7d7-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8e7d7-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="8e7d7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e7d7-136">NOTES</span></span>

## <span data-ttu-id="8e7d7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e7d7-137">RELATED LINKS</span></span>
