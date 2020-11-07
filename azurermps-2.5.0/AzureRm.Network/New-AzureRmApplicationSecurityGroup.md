---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 99c863861bdf6a434e1268dcb1d9dd55ff8d9f80
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848416"
---
# <span data-ttu-id="fc7c5-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc7c5-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="fc7c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7c5-103">Erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc7c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc7c5-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="fc7c5-106">Das Cmdlet **New-AzureRmApplicationSecurityGroup** erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="fc7c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="fc7c5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc7c5-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="fc7c5-109">In diesem Beispiel wird eine Anwendungs Sicherheitsgruppe ohne Zuordnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="fc7c5-110">Nach der Erstellung können IP-Konfigurationen in der Netzwerkschnittstelle in die Gruppe aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="fc7c5-111">Sicherheitsregeln können auch auf die Gruppe als ihre Quellen oder Ziele verweisen.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="fc7c5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc7c5-112">PARAMETERS</span></span>

### <span data-ttu-id="fc7c5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc7c5-113">-AsJob</span></span>
<span data-ttu-id="fc7c5-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fc7c5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc7c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7c5-115">-DefaultProfile</span></span>
<span data-ttu-id="fc7c5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc7c5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fc7c5-117">-Force</span></span>
<span data-ttu-id="fc7c5-118">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="fc7c5-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="fc7c5-119">-Location</span></span>
<span data-ttu-id="fc7c5-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7c5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fc7c5-121">-Name</span></span>
<span data-ttu-id="fc7c5-122">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc7c5-124">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-124">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7c5-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc7c5-125">-Tag</span></span>
<span data-ttu-id="fc7c5-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fc7c5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc7c5-127">-Confirm</span></span>
<span data-ttu-id="fc7c5-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc7c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7c5-129">-WhatIf</span></span>
<span data-ttu-id="fc7c5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7c5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc7c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7c5-132">CommonParameters</span></span>
<span data-ttu-id="fc7c5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7c5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc7c5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7c5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc7c5-135">INPUTS</span></span>

### <span data-ttu-id="fc7c5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fc7c5-136">System.String</span></span>
<span data-ttu-id="fc7c5-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc7c5-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc7c5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc7c5-138">OUTPUTS</span></span>

### <span data-ttu-id="fc7c5-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc7c5-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="fc7c5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc7c5-140">NOTES</span></span>

## <span data-ttu-id="fc7c5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc7c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="fc7c5-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc7c5-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="fc7c5-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc7c5-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="fc7c5-144">Neu – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc7c5-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fc7c5-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc7c5-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fc7c5-146">Satz-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc7c5-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fc7c5-147">Neu – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc7c5-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fc7c5-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc7c5-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fc7c5-149">Satz-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc7c5-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
