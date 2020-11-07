---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664250"
---
# <span data-ttu-id="3d42f-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d42f-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="3d42f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d42f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d42f-103">Erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d42f-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d42f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d42f-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d42f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d42f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d42f-106">Das Cmdlet **New-AzureRmApplicationSecurityGroup** erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d42f-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="3d42f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d42f-107">EXAMPLES</span></span>

### <span data-ttu-id="3d42f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d42f-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="3d42f-109">In diesem Beispiel wird eine Anwendungs Sicherheitsgruppe ohne Zuordnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d42f-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="3d42f-110">Nach der Erstellung können IP-Konfigurationen in der Netzwerkschnittstelle in die Gruppe aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="3d42f-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="3d42f-111">Sicherheitsregeln können auch auf die Gruppe als ihre Quellen oder Ziele verweisen.</span><span class="sxs-lookup"><span data-stu-id="3d42f-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="3d42f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d42f-112">PARAMETERS</span></span>

### <span data-ttu-id="3d42f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d42f-113">-DefaultProfile</span></span>
<span data-ttu-id="3d42f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d42f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d42f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3d42f-115">-Force</span></span>
<span data-ttu-id="3d42f-116">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="3d42f-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="3d42f-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="3d42f-117">-Location</span></span>
<span data-ttu-id="3d42f-118">Die Position.</span><span class="sxs-lookup"><span data-stu-id="3d42f-118">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d42f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3d42f-119">-Name</span></span>
<span data-ttu-id="3d42f-120">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d42f-120">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d42f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d42f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d42f-122">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d42f-122">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d42f-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d42f-123">-Tag</span></span>
<span data-ttu-id="3d42f-124">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d42f-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3d42f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d42f-125">-Confirm</span></span>
<span data-ttu-id="3d42f-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d42f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d42f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d42f-127">-WhatIf</span></span>
<span data-ttu-id="3d42f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d42f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d42f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d42f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d42f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d42f-130">CommonParameters</span></span>
<span data-ttu-id="3d42f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d42f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d42f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d42f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d42f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d42f-133">INPUTS</span></span>

### <span data-ttu-id="3d42f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3d42f-134">System.String</span></span>
<span data-ttu-id="3d42f-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d42f-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d42f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d42f-136">OUTPUTS</span></span>

### <span data-ttu-id="3d42f-137">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d42f-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="3d42f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d42f-138">NOTES</span></span>

## <span data-ttu-id="3d42f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d42f-139">RELATED LINKS</span></span>

[<span data-ttu-id="3d42f-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d42f-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="3d42f-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d42f-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="3d42f-142">Neu – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3d42f-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3d42f-144">Satz-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3d42f-145">Neu – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3d42f-146">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3d42f-147">Satz-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
