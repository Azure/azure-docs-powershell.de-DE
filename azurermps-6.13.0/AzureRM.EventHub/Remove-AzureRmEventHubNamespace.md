---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496205"
---
# <span data-ttu-id="d1cb1-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d1cb1-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="d1cb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cb1-103">Entfernt den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1cb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1cb1-104">SYNTAX</span></span>

### <span data-ttu-id="d1cb1-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1cb1-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cb1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1cb1-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1cb1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1cb1-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1cb1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1cb1-108">DESCRIPTION</span></span>
<span data-ttu-id="d1cb1-109">Das Remove-AzureRmEventHubNamespace-Cmdlet entfernt den angegebenen Event Hubs-Namespace und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="d1cb1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1cb1-110">EXAMPLES</span></span>

### <span data-ttu-id="d1cb1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1cb1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="d1cb1-112">Entfernt den Event Hubs \` -Namespace mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d1cb1-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d1cb1-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="d1cb1-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="d1cb1-114">Beispiel 2,1-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="d1cb1-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="d1cb1-115">Beispiel 3,1-Resourcen-using-Variable</span><span class="sxs-lookup"><span data-stu-id="d1cb1-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="d1cb1-116">Beispiel 3,2-Resourcen-using-Piping:</span><span class="sxs-lookup"><span data-stu-id="d1cb1-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="d1cb1-117">Beispiel 3,3-Resourcen-using-Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="d1cb1-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="d1cb1-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1cb1-118">PARAMETERS</span></span>

### <span data-ttu-id="d1cb1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1cb1-119">-AsJob</span></span>
<span data-ttu-id="d1cb1-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d1cb1-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cb1-121">-DefaultProfile</span></span>
<span data-ttu-id="d1cb1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1cb1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1cb1-123">-InputObject</span></span>
<span data-ttu-id="d1cb1-124">EventHubs-Namespace Objekt</span><span class="sxs-lookup"><span data-stu-id="d1cb1-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d1cb1-125">-Name</span></span>
<span data-ttu-id="d1cb1-126">EventHub-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d1cb1-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1cb1-127">-PassThru</span></span>
<span data-ttu-id="d1cb1-128">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-128">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1cb1-129">-ResourceGroupName</span></span>
<span data-ttu-id="d1cb1-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d1cb1-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb1-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1cb1-131">-ResourceId</span></span>
<span data-ttu-id="d1cb1-132">EventHubs-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d1cb1-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cb1-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1cb1-133">-Confirm</span></span>
<span data-ttu-id="d1cb1-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1cb1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1cb1-135">-WhatIf</span></span>
<span data-ttu-id="d1cb1-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1cb1-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1cb1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cb1-138">CommonParameters</span></span>
<span data-ttu-id="d1cb1-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cb1-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1cb1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cb1-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1cb1-141">INPUTS</span></span>

### <span data-ttu-id="d1cb1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d1cb1-142">System.String</span></span>

### <span data-ttu-id="d1cb1-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d1cb1-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="d1cb1-144">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1cb1-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d1cb1-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1cb1-145">OUTPUTS</span></span>

### <span data-ttu-id="d1cb1-146">System. void</span><span class="sxs-lookup"><span data-stu-id="d1cb1-146">System.Void</span></span>

## <span data-ttu-id="d1cb1-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1cb1-147">NOTES</span></span>

## <span data-ttu-id="d1cb1-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1cb1-148">RELATED LINKS</span></span>
