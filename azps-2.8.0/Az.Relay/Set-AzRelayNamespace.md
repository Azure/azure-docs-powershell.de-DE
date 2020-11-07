---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: eb42dc22f972928405821e8468e5610fa9c4514f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823580"
---
# <span data-ttu-id="128b9-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="128b9-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="128b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="128b9-102">SYNOPSIS</span></span>
<span data-ttu-id="128b9-103">Aktualisiert die Beschreibung eines vorhandenen Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="128b9-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="128b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="128b9-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="128b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="128b9-105">DESCRIPTION</span></span>
<span data-ttu-id="128b9-106">Das Cmdlet " **Satz-AzRelayNamespace** " aktualisiert die Beschreibung des angegebenen Relay-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="128b9-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="128b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="128b9-107">EXAMPLES</span></span>

### <span data-ttu-id="128b9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="128b9-108">Example 1</span></span>
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

<span data-ttu-id="128b9-109">Aktualisiert den Relay-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="128b9-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="128b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="128b9-110">PARAMETERS</span></span>

### <span data-ttu-id="128b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128b9-111">-DefaultProfile</span></span>
<span data-ttu-id="128b9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="128b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128b9-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="128b9-113">-InputObject</span></span>
<span data-ttu-id="128b9-114">Relay-Namespace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="128b9-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="128b9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="128b9-115">-Name</span></span>
<span data-ttu-id="128b9-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="128b9-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="128b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="128b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="128b9-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="128b9-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="128b9-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="128b9-119">-Tag</span></span>
<span data-ttu-id="128b9-120">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="128b9-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="128b9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="128b9-121">-Confirm</span></span>
<span data-ttu-id="128b9-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="128b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="128b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="128b9-123">-WhatIf</span></span>
<span data-ttu-id="128b9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="128b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="128b9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="128b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="128b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128b9-126">CommonParameters</span></span>
<span data-ttu-id="128b9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="128b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128b9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="128b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128b9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="128b9-129">INPUTS</span></span>

### <span data-ttu-id="128b9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="128b9-130">System.String</span></span>

### <span data-ttu-id="128b9-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="128b9-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="128b9-132">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="128b9-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="128b9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="128b9-133">OUTPUTS</span></span>

### <span data-ttu-id="128b9-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="128b9-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="128b9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="128b9-135">NOTES</span></span>

## <span data-ttu-id="128b9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="128b9-136">RELATED LINKS</span></span>
