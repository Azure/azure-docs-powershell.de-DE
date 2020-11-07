---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a3f2c76de9dc331c6b073f724fede6a3bafeed18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650716"
---
# <span data-ttu-id="11137-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11137-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="11137-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11137-102">SYNOPSIS</span></span>
<span data-ttu-id="11137-103">Ändert eine Integration-Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="11137-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11137-104">SYNTAX</span></span>

### <span data-ttu-id="11137-105">ByIntegrationAccountAndFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="11137-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="11137-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11137-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="11137-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11137-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="11137-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="11137-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="11137-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="11137-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="11137-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="11137-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11137-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11137-114">DESCRIPTION</span></span>
<span data-ttu-id="11137-115">Das Cmdlet " **Satz-AzIntegrationAccountAssembly** " ändert eine Integration-Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="11137-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11137-116">EXAMPLES</span></span>

### <span data-ttu-id="11137-117">Beispiel 1: Ändern einer Assembly mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="11137-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="11137-118">Ändert die Assembly mit dem Namen "SampleAssembly" unter Verwendung der lokalen Datei, die sich im Dateipfad befindet, der in "$localAssemblyFilePath" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="11137-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="11137-119">Beispiel 2: Ändern einer Assembly mithilfe von Bytedaten</span><span class="sxs-lookup"><span data-stu-id="11137-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="11137-120">Ändert die Assembly mit dem Namen "SampleAssembly" mit einem Byte-Array, das in "$assemblyContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="11137-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="11137-121">Beispiel 3: Ändern einer Assembly mithilfe eines Inhaltslinks</span><span class="sxs-lookup"><span data-stu-id="11137-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="11137-122">Ändert die Assembly mit dem Namen "SampleAssembly" mit den Byte-Daten, die sich unter der URL "$assemblyUrl" befinden.</span><span class="sxs-lookup"><span data-stu-id="11137-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="11137-123">Dies ist die empfohlene Methode zum Erstellen von großformatigen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="11137-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="11137-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="11137-124">PARAMETERS</span></span>

### <span data-ttu-id="11137-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="11137-125">-AssemblyData</span></span>
<span data-ttu-id="11137-126">Die Bytedaten der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="11137-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="11137-127">-AssemblyFilePath</span></span>
<span data-ttu-id="11137-128">Der Dateipfad der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="11137-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="11137-129">-ContentLink</span></span>
<span data-ttu-id="11137-130">Ein öffentlich zugänglicher Link zu den Assemblydaten des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="11137-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="11137-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11137-131">-DefaultProfile</span></span>
<span data-ttu-id="11137-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11137-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11137-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11137-133">-InputObject</span></span>
<span data-ttu-id="11137-134">Eine Integration Account-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11137-135">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="11137-135">-Metadata</span></span>
<span data-ttu-id="11137-136">Die Metadaten für die Integrations Konto-Assembly</span><span class="sxs-lookup"><span data-stu-id="11137-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="11137-137">-Name</span><span class="sxs-lookup"><span data-stu-id="11137-137">-Name</span></span>
<span data-ttu-id="11137-138">Der Name der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11137-139">-Übergeordneter</span><span class="sxs-lookup"><span data-stu-id="11137-139">-ParentName</span></span>
<span data-ttu-id="11137-140">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="11137-140">The integration account name.</span></span>

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

### <span data-ttu-id="11137-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11137-141">-ResourceGroupName</span></span>
<span data-ttu-id="11137-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="11137-142">The resource group name.</span></span>

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

### <span data-ttu-id="11137-143">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="11137-143">-ResourceId</span></span>
<span data-ttu-id="11137-144">Die Ressourcen-ID der Integrations Konto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="11137-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="11137-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11137-145">-Confirm</span></span>
<span data-ttu-id="11137-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11137-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11137-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11137-147">-WhatIf</span></span>
<span data-ttu-id="11137-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11137-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11137-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11137-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11137-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11137-150">CommonParameters</span></span>
<span data-ttu-id="11137-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11137-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11137-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11137-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11137-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11137-153">INPUTS</span></span>

### <span data-ttu-id="11137-154">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11137-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="11137-155">System. String</span><span class="sxs-lookup"><span data-stu-id="11137-155">System.String</span></span>

## <span data-ttu-id="11137-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11137-156">OUTPUTS</span></span>

### <span data-ttu-id="11137-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11137-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="11137-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="11137-158">NOTES</span></span>

## <span data-ttu-id="11137-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11137-159">RELATED LINKS</span></span>
