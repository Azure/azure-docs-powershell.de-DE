---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 0da9ecf9fabaa1cbb21a5fe8f82bb172b84850e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662738"
---
# <span data-ttu-id="82980-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="82980-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="82980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82980-102">SYNOPSIS</span></span>
<span data-ttu-id="82980-103">Ruft Geo Dr-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="82980-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82980-104">SYNTAX</span></span>

### <span data-ttu-id="82980-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="82980-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82980-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82980-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82980-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82980-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82980-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82980-108">DESCRIPTION</span></span>
<span data-ttu-id="82980-109">Das Cmdlet " **Satz-AzureRmEventHubGeoDRConfigurationFailOver** " envokes Geo Dr-Failover, und konfigurieren Sie den Alias so, dass er auf den sekundären Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="82980-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="82980-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82980-110">EXAMPLES</span></span>

### <span data-ttu-id="82980-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82980-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="82980-112">Ruft das Failover für den Alias "SampleDRCongifName" auf, konfiguriert und verweist auf den sekundären Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="82980-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="82980-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="82980-113">PARAMETERS</span></span>

### <span data-ttu-id="82980-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82980-114">-DefaultProfile</span></span>
<span data-ttu-id="82980-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82980-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82980-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="82980-116">-InputObject</span></span>
<span data-ttu-id="82980-117">Eventhub GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="82980-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82980-118">-Name</span><span class="sxs-lookup"><span data-stu-id="82980-118">-Name</span></span>
<span data-ttu-id="82980-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="82980-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82980-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="82980-120">-Namespace</span></span>
<span data-ttu-id="82980-121">Namespace Name – sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="82980-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82980-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82980-122">-PassThru</span></span>
<span data-ttu-id="82980-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="82980-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82980-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="82980-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82980-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82980-125">-ResourceGroupName</span></span>
<span data-ttu-id="82980-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="82980-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82980-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="82980-127">-ResourceId</span></span>
<span data-ttu-id="82980-128">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="82980-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82980-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82980-129">-Confirm</span></span>
<span data-ttu-id="82980-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82980-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82980-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82980-131">-WhatIf</span></span>
<span data-ttu-id="82980-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82980-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82980-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82980-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82980-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82980-134">CommonParameters</span></span>
<span data-ttu-id="82980-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82980-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="82980-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82980-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82980-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82980-137">INPUTS</span></span>

### <span data-ttu-id="82980-138">System. String</span><span class="sxs-lookup"><span data-stu-id="82980-138">System.String</span></span>
<span data-ttu-id="82980-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="82980-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="82980-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82980-140">OUTPUTS</span></span>

### <span data-ttu-id="82980-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82980-141">System.Boolean</span></span>


## <span data-ttu-id="82980-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="82980-142">NOTES</span></span>

## <span data-ttu-id="82980-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82980-143">RELATED LINKS</span></span>
