---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a52d1d44647d2b608a34a07722439f243ba08510
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947032"
---
# <span data-ttu-id="5deab-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5deab-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5deab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5deab-102">SYNOPSIS</span></span>
<span data-ttu-id="5deab-103">Erstellt eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="5deab-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="5deab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5deab-104">SYNTAX</span></span>

### <span data-ttu-id="5deab-105">ByIntegrationAccountAndFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="5deab-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deab-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5deab-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5deab-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5deab-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5deab-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5deab-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deab-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5deab-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deab-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5deab-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deab-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5deab-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deab-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5deab-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5deab-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5deab-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5deab-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5deab-114">DESCRIPTION</span></span>
<span data-ttu-id="5deab-115">Das **Get-AzIntegrationAccountAssembly-Cmdlet** erstellt eine neue Assembly in einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="5deab-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="5deab-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5deab-116">EXAMPLES</span></span>

### <span data-ttu-id="5deab-117">Beispiel 1: Erstellen einer neuen Assembly mit einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="5deab-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5deab-118">Erstellt eine neue Assembly mit der lokalen Datei, die sich im Dateipfad befindet, der in "$localAssemblyFilePath" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5deab-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="5deab-119">Beispiel 2: Erstellen einer neuen Assembly mithilfe von Bytedaten</span><span class="sxs-lookup"><span data-stu-id="5deab-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5deab-120">Erstellt eine neue Assembly mit dem byte-Array, das in "$assemblyContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5deab-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="5deab-121">Beispiel 3: Erstellen einer neuen Assembly mithilfe eines Inhaltslinks</span><span class="sxs-lookup"><span data-stu-id="5deab-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5deab-122">Erstellt eine neue Assembly mit den Bytedaten, die sich unter der URL "$assemblyUrl" befinden.</span><span class="sxs-lookup"><span data-stu-id="5deab-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="5deab-123">Dies ist die vorgeschlagene Methode zum Erstellen großer Assemblys.</span><span class="sxs-lookup"><span data-stu-id="5deab-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="5deab-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5deab-124">PARAMETERS</span></span>

### <span data-ttu-id="5deab-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="5deab-125">-AssemblyData</span></span>
<span data-ttu-id="5deab-126">Die Bytedaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="5deab-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="5deab-127">-AssemblyFilePath</span></span>
<span data-ttu-id="5deab-128">Der Dateipfad der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="5deab-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="5deab-129">-ContentLink</span></span>
<span data-ttu-id="5deab-130">Ein öffentlich zugänglicher Link zu den Assemblydaten des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5deab-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5deab-131">-DefaultProfile</span></span>
<span data-ttu-id="5deab-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5deab-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5deab-133">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="5deab-133">-Metadata</span></span>
<span data-ttu-id="5deab-134">Die Metadaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="5deab-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-135">-Name</span><span class="sxs-lookup"><span data-stu-id="5deab-135">-Name</span></span>
<span data-ttu-id="5deab-136">Der Assemblyname des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5deab-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5deab-137">-ParentName</span></span>
<span data-ttu-id="5deab-138">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5deab-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5deab-139">-ParentObject</span></span>
<span data-ttu-id="5deab-140">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="5deab-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5deab-141">-ParentResourceId</span></span>
<span data-ttu-id="5deab-142">Die Ressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="5deab-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5deab-143">-ResourceGroupName</span></span>
<span data-ttu-id="5deab-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5deab-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5deab-145">-Confirm</span></span>
<span data-ttu-id="5deab-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5deab-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5deab-147">-WhatIf</span></span>
<span data-ttu-id="5deab-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5deab-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5deab-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5deab-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5deab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5deab-150">CommonParameters</span></span>
<span data-ttu-id="5deab-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5deab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5deab-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5deab-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5deab-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5deab-153">INPUTS</span></span>

### <span data-ttu-id="5deab-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5deab-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="5deab-155">System.String</span><span class="sxs-lookup"><span data-stu-id="5deab-155">System.String</span></span>

## <span data-ttu-id="5deab-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5deab-156">OUTPUTS</span></span>

### <span data-ttu-id="5deab-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5deab-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5deab-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5deab-158">NOTES</span></span>

## <span data-ttu-id="5deab-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5deab-159">RELATED LINKS</span></span>
