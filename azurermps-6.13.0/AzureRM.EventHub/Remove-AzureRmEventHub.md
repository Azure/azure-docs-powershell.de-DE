---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499510"
---
# <span data-ttu-id="a5b85-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="a5b85-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="a5b85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5b85-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b85-103">Entfernt den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="a5b85-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5b85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5b85-104">SYNTAX</span></span>

### <span data-ttu-id="a5b85-105">EventhubDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5b85-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b85-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5b85-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b85-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b85-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b85-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5b85-108">DESCRIPTION</span></span>
<span data-ttu-id="a5b85-109">Das Remove-AzureRmEventHub-Cmdlet entfernt und löscht den angegebenen Ereignis-Hub aus dem angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="a5b85-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="a5b85-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5b85-110">EXAMPLES</span></span>

### <span data-ttu-id="a5b85-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5b85-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="a5b85-112">Entfernt den Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="a5b85-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="a5b85-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="a5b85-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="a5b85-114">Beispiel 2,2-Inputobject mit Piping:</span><span class="sxs-lookup"><span data-stu-id="a5b85-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="a5b85-115">Beispiel 3,1-Resourcen-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="a5b85-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="a5b85-116">Beispiel 3,1-Resourcen-using-Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="a5b85-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="a5b85-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5b85-117">PARAMETERS</span></span>

### <span data-ttu-id="a5b85-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5b85-118">-AsJob</span></span>
<span data-ttu-id="a5b85-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a5b85-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5b85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b85-120">-DefaultProfile</span></span>
<span data-ttu-id="a5b85-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5b85-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b85-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5b85-122">-InputObject</span></span>
<span data-ttu-id="a5b85-123">Eventhub-Objekt</span><span class="sxs-lookup"><span data-stu-id="a5b85-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b85-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a5b85-124">-Name</span></span>
<span data-ttu-id="a5b85-125">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="a5b85-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b85-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5b85-126">-Namespace</span></span>
<span data-ttu-id="a5b85-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a5b85-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b85-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5b85-128">-PassThru</span></span>
<span data-ttu-id="a5b85-129">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a5b85-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a5b85-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b85-130">-ResourceGroupName</span></span>
<span data-ttu-id="a5b85-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a5b85-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b85-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5b85-132">-ResourceId</span></span>
<span data-ttu-id="a5b85-133">Eventhub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a5b85-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b85-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5b85-134">-Confirm</span></span>
<span data-ttu-id="a5b85-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5b85-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b85-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b85-136">-WhatIf</span></span>
<span data-ttu-id="a5b85-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5b85-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b85-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5b85-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b85-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b85-139">CommonParameters</span></span>
<span data-ttu-id="a5b85-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b85-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b85-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b85-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b85-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5b85-142">INPUTS</span></span>

### <span data-ttu-id="a5b85-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b85-143">System.String</span></span>

### <span data-ttu-id="a5b85-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a5b85-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="a5b85-145">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5b85-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a5b85-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5b85-146">OUTPUTS</span></span>

### <span data-ttu-id="a5b85-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5b85-147">System.Boolean</span></span>

## <span data-ttu-id="a5b85-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5b85-148">NOTES</span></span>

## <span data-ttu-id="a5b85-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5b85-149">RELATED LINKS</span></span>
