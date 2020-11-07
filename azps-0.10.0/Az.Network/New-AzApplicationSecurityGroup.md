---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 81eaa1f5c6e44586ae6ac9e5b6838f00063a9211
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841371"
---
# <span data-ttu-id="990b8-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="990b8-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="990b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="990b8-102">SYNOPSIS</span></span>
<span data-ttu-id="990b8-103">Erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="990b8-103">Creates an application security group.</span></span>

## <span data-ttu-id="990b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="990b8-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="990b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="990b8-105">DESCRIPTION</span></span>
<span data-ttu-id="990b8-106">Das Cmdlet **New-AzApplicationSecurityGroup** erstellt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="990b8-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="990b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="990b8-107">EXAMPLES</span></span>

### <span data-ttu-id="990b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="990b8-108">Example 1</span></span>
```
PS C:\> New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="990b8-109">In diesem Beispiel wird eine Anwendungs Sicherheitsgruppe ohne Zuordnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="990b8-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="990b8-110">Nach der Erstellung können IP-Konfigurationen in der Netzwerkschnittstelle in die Gruppe aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="990b8-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="990b8-111">Sicherheitsregeln können auch auf die Gruppe als ihre Quellen oder Ziele verweisen.</span><span class="sxs-lookup"><span data-stu-id="990b8-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="990b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="990b8-112">PARAMETERS</span></span>

### <span data-ttu-id="990b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="990b8-113">-AsJob</span></span>
<span data-ttu-id="990b8-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="990b8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="990b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990b8-115">-DefaultProfile</span></span>
<span data-ttu-id="990b8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="990b8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="990b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="990b8-117">-Force</span></span>
<span data-ttu-id="990b8-118">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="990b8-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="990b8-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="990b8-119">-Location</span></span>
<span data-ttu-id="990b8-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="990b8-120">The location.</span></span>

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

### <span data-ttu-id="990b8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="990b8-121">-Name</span></span>
<span data-ttu-id="990b8-122">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="990b8-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="990b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="990b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="990b8-124">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="990b8-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="990b8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="990b8-125">-Tag</span></span>
<span data-ttu-id="990b8-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="990b8-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="990b8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="990b8-127">-Confirm</span></span>
<span data-ttu-id="990b8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="990b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="990b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="990b8-129">-WhatIf</span></span>
<span data-ttu-id="990b8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="990b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="990b8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="990b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="990b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990b8-132">CommonParameters</span></span>
<span data-ttu-id="990b8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="990b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990b8-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="990b8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990b8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="990b8-135">INPUTS</span></span>

### <span data-ttu-id="990b8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="990b8-136">System.String</span></span>
<span data-ttu-id="990b8-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="990b8-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="990b8-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="990b8-138">OUTPUTS</span></span>

### <span data-ttu-id="990b8-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="990b8-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="990b8-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="990b8-140">NOTES</span></span>

## <span data-ttu-id="990b8-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="990b8-141">RELATED LINKS</span></span>

[<span data-ttu-id="990b8-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="990b8-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="990b8-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="990b8-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="990b8-144">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="990b8-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="990b8-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="990b8-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="990b8-146">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="990b8-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="990b8-147">Neu – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="990b8-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="990b8-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="990b8-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="990b8-149">Satz-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="990b8-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
