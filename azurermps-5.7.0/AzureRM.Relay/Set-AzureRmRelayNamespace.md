---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 09c601e2ecfddf417e90efd60b58bcdd1a51ff5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480982"
---
# <span data-ttu-id="65847-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="65847-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="65847-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65847-102">SYNOPSIS</span></span>
<span data-ttu-id="65847-103">Aktualisiert die Beschreibung eines vorhandenen Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="65847-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65847-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65847-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65847-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65847-105">DESCRIPTION</span></span>
<span data-ttu-id="65847-106">Das Cmdlet " **Satz-AzureRmRelayNamespace** " aktualisiert die Beschreibung des angegebenen Relay-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65847-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="65847-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65847-107">EXAMPLES</span></span>

### <span data-ttu-id="65847-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65847-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="65847-109">Aktualisiert den Relay-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="65847-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="65847-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65847-110">PARAMETERS</span></span>

### <span data-ttu-id="65847-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65847-111">-DefaultProfile</span></span>
<span data-ttu-id="65847-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65847-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65847-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65847-113">-InputObject</span></span>
<span data-ttu-id="65847-114">Relay-Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="65847-114">Relay Namespace object</span></span>

```yaml
Type: RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65847-115">-Name</span><span class="sxs-lookup"><span data-stu-id="65847-115">-Name</span></span>
<span data-ttu-id="65847-116">Name des Relay-Namespaces</span><span class="sxs-lookup"><span data-stu-id="65847-116">Relay Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65847-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65847-117">-ResourceGroupName</span></span>
<span data-ttu-id="65847-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65847-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65847-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="65847-119">-Tag</span></span>
<span data-ttu-id="65847-120">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="65847-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65847-121">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="65847-121">For example:</span></span>

<span data-ttu-id="65847-122">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="65847-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65847-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65847-123">-Confirm</span></span>
<span data-ttu-id="65847-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65847-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65847-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65847-125">-WhatIf</span></span>
<span data-ttu-id="65847-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65847-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65847-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65847-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65847-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65847-128">CommonParameters</span></span>
<span data-ttu-id="65847-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65847-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65847-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65847-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65847-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65847-131">INPUTS</span></span>

### <span data-ttu-id="65847-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65847-132">-ResourceGroupName</span></span>
 <span data-ttu-id="65847-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65847-133">System.String</span></span>

### <span data-ttu-id="65847-134">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="65847-134">-NamespaceName</span></span>
 <span data-ttu-id="65847-135">System. String</span><span class="sxs-lookup"><span data-stu-id="65847-135">System.String</span></span>

### <span data-ttu-id="65847-136">-Standort</span><span class="sxs-lookup"><span data-stu-id="65847-136">-Location</span></span>
 <span data-ttu-id="65847-137">System. String</span><span class="sxs-lookup"><span data-stu-id="65847-137">System.String</span></span>

### <span data-ttu-id="65847-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="65847-138">-Tag</span></span>
 <span data-ttu-id="65847-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65847-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65847-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65847-140">OUTPUTS</span></span>

### <span data-ttu-id="65847-141">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="65847-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="65847-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="65847-142">NOTES</span></span>

## <span data-ttu-id="65847-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65847-143">RELATED LINKS</span></span>

