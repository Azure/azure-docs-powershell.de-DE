---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007973"
---
# <span data-ttu-id="687cc-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="687cc-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="687cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="687cc-102">SYNOPSIS</span></span>
<span data-ttu-id="687cc-103">Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="687cc-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="687cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="687cc-104">SYNTAX</span></span>

### <span data-ttu-id="687cc-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="687cc-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687cc-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="687cc-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687cc-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="687cc-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687cc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="687cc-108">DESCRIPTION</span></span>
<span data-ttu-id="687cc-109">Das Cmdlet " **festlegen-AzEventHubGeoDRConfigurationBreakPair** " deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="687cc-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="687cc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="687cc-110">EXAMPLES</span></span>

### <span data-ttu-id="687cc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="687cc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="687cc-112">Dieser Vorgang deaktiviert die Disaster Recovery und beendet die Replikation von Änderungen von primären zu sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="687cc-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="687cc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="687cc-113">PARAMETERS</span></span>

### <span data-ttu-id="687cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687cc-114">-DefaultProfile</span></span>
<span data-ttu-id="687cc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="687cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687cc-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="687cc-116">-InputObject</span></span>
<span data-ttu-id="687cc-117">Eventhub GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="687cc-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="687cc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="687cc-118">-Name</span></span>
<span data-ttu-id="687cc-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="687cc-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687cc-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="687cc-120">-Namespace</span></span>
<span data-ttu-id="687cc-121">Namespace Name – primärer Namespace</span><span class="sxs-lookup"><span data-stu-id="687cc-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687cc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="687cc-122">-PassThru</span></span>
<span data-ttu-id="687cc-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="687cc-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="687cc-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="687cc-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="687cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="687cc-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="687cc-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687cc-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="687cc-127">-ResourceId</span></span>
<span data-ttu-id="687cc-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="687cc-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687cc-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="687cc-129">-Confirm</span></span>
<span data-ttu-id="687cc-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="687cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687cc-131">-WhatIf</span></span>
<span data-ttu-id="687cc-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="687cc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="687cc-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="687cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687cc-134">CommonParameters</span></span>
<span data-ttu-id="687cc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="687cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687cc-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="687cc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687cc-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="687cc-137">INPUTS</span></span>

### <span data-ttu-id="687cc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="687cc-138">System.String</span></span>

### <span data-ttu-id="687cc-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="687cc-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="687cc-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="687cc-140">OUTPUTS</span></span>

### <span data-ttu-id="687cc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="687cc-141">System.Boolean</span></span>

## <span data-ttu-id="687cc-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="687cc-142">NOTES</span></span>

## <span data-ttu-id="687cc-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="687cc-143">RELATED LINKS</span></span>
