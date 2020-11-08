---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007877"
---
# <span data-ttu-id="3f1a8-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="3f1a8-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="3f1a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1a8-103">Aktualisiert die Beschreibung eines vorhandenen Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="3f1a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f1a8-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f1a8-105">DESCRIPTION</span></span>
<span data-ttu-id="3f1a8-106">Das Cmdlet " **Satz-AzRelayNamespace** " aktualisiert die Beschreibung des angegebenen Relay-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="3f1a8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f1a8-107">EXAMPLES</span></span>

### <span data-ttu-id="3f1a8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f1a8-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="3f1a8-109">Aktualisiert den Relay-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="3f1a8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f1a8-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1a8-111">-DefaultProfile</span></span>
<span data-ttu-id="3f1a8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f1a8-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3f1a8-113">-InputObject</span></span>
<span data-ttu-id="3f1a8-114">Relay-Namespace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3f1a8-115">-Name</span></span>
<span data-ttu-id="3f1a8-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f1a8-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a8-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f1a8-119">-Tag</span></span>
<span data-ttu-id="3f1a8-120">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-120">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1a8-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f1a8-121">-Confirm</span></span>
<span data-ttu-id="3f1a8-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1a8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1a8-123">-WhatIf</span></span>
<span data-ttu-id="3f1a8-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1a8-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1a8-126">CommonParameters</span></span>
<span data-ttu-id="3f1a8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1a8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1a8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f1a8-129">INPUTS</span></span>

### <span data-ttu-id="3f1a8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3f1a8-130">System.String</span></span>

### <span data-ttu-id="3f1a8-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3f1a8-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3f1a8-132">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="3f1a8-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="3f1a8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f1a8-133">OUTPUTS</span></span>

### <span data-ttu-id="3f1a8-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3f1a8-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="3f1a8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f1a8-135">NOTES</span></span>

## <span data-ttu-id="3f1a8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f1a8-136">RELATED LINKS</span></span>
