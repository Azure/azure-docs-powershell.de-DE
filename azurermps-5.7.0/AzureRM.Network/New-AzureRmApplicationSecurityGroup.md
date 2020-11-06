---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 82fdec48f2e021e33490f84a05a064fb007ac8d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479686"
---
# <span data-ttu-id="275ea-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="275ea-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="275ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="275ea-102">SYNOPSIS</span></span>
<span data-ttu-id="275ea-103">Erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="275ea-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="275ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="275ea-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="275ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="275ea-105">DESCRIPTION</span></span>
<span data-ttu-id="275ea-106">Das Cmdlet **New-AzureRmApplicationSecurityGroup** erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="275ea-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="275ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="275ea-107">EXAMPLES</span></span>

### <span data-ttu-id="275ea-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="275ea-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="275ea-109">In diesem Beispiel wird eine Anwendungs Sicherheitsgruppe ohne Zuordnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="275ea-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="275ea-110">Nach der Erstellung können IP-Konfigurationen in der Netzwerkschnittstelle in die Gruppe aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="275ea-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="275ea-111">Sicherheitsregeln können auch auf die Gruppe als ihre Quellen oder Ziele verweisen.</span><span class="sxs-lookup"><span data-stu-id="275ea-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="275ea-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="275ea-112">PARAMETERS</span></span>

### <span data-ttu-id="275ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="275ea-113">-AsJob</span></span>
<span data-ttu-id="275ea-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="275ea-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="275ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275ea-115">-DefaultProfile</span></span>
<span data-ttu-id="275ea-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="275ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="275ea-117">-Force</span><span class="sxs-lookup"><span data-stu-id="275ea-117">-Force</span></span>
<span data-ttu-id="275ea-118">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="275ea-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="275ea-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="275ea-119">-Location</span></span>
<span data-ttu-id="275ea-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="275ea-120">The location.</span></span>

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

### <span data-ttu-id="275ea-121">-Name</span><span class="sxs-lookup"><span data-stu-id="275ea-121">-Name</span></span>
<span data-ttu-id="275ea-122">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="275ea-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="275ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="275ea-124">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="275ea-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="275ea-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="275ea-125">-Tag</span></span>
<span data-ttu-id="275ea-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="275ea-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="275ea-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="275ea-127">-Confirm</span></span>
<span data-ttu-id="275ea-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="275ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275ea-129">-WhatIf</span></span>
<span data-ttu-id="275ea-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="275ea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275ea-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="275ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275ea-132">CommonParameters</span></span>
<span data-ttu-id="275ea-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275ea-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275ea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275ea-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="275ea-135">INPUTS</span></span>

### <span data-ttu-id="275ea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="275ea-136">System.String</span></span>
<span data-ttu-id="275ea-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="275ea-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="275ea-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="275ea-138">OUTPUTS</span></span>

### <span data-ttu-id="275ea-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="275ea-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="275ea-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="275ea-140">NOTES</span></span>

## <span data-ttu-id="275ea-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="275ea-141">RELATED LINKS</span></span>

[<span data-ttu-id="275ea-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="275ea-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="275ea-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="275ea-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="275ea-144">Neu – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="275ea-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="275ea-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="275ea-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="275ea-146">Satz-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="275ea-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="275ea-147">Neu – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="275ea-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="275ea-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="275ea-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="275ea-149">Satz-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="275ea-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
