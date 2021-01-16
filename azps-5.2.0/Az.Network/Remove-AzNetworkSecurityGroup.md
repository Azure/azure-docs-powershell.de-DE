---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301915"
---
# <span data-ttu-id="24635-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24635-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="24635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24635-102">SYNOPSIS</span></span>
<span data-ttu-id="24635-103">Entfernt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="24635-103">Removes a network security group.</span></span>

## <span data-ttu-id="24635-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24635-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24635-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24635-105">DESCRIPTION</span></span>
<span data-ttu-id="24635-106">Das **Cmdlet "Remove-AzNetworkSecurityGroup"** entfernt eine Azure-Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="24635-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="24635-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24635-107">EXAMPLES</span></span>

### <span data-ttu-id="24635-108">Beispiel 1: Entfernen einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="24635-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="24635-109">Mit diesem Befehl wird die Sicherheitsgruppe namens NSG-FrontEnd in der Ressourcengruppe "TestRG" entfernt.</span><span class="sxs-lookup"><span data-stu-id="24635-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="24635-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24635-110">PARAMETERS</span></span>

### <span data-ttu-id="24635-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24635-111">-AsJob</span></span>
<span data-ttu-id="24635-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="24635-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24635-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24635-113">-DefaultProfile</span></span>
<span data-ttu-id="24635-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24635-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24635-115">-Force</span><span class="sxs-lookup"><span data-stu-id="24635-115">-Force</span></span>
<span data-ttu-id="24635-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="24635-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24635-117">-Name</span><span class="sxs-lookup"><span data-stu-id="24635-117">-Name</span></span>
<span data-ttu-id="24635-118">Gibt den Namen der Netzwerksicherheitsgruppe an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="24635-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="24635-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24635-119">-PassThru</span></span>
<span data-ttu-id="24635-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="24635-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="24635-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="24635-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="24635-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24635-122">-ResourceGroupName</span></span>
<span data-ttu-id="24635-123">Gibt den Namen einer Ressourcengruppe an, aus der mit diesem Cmdlet eine Netzwerksicherheitsgruppe entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="24635-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="24635-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24635-124">-Confirm</span></span>
<span data-ttu-id="24635-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24635-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24635-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="24635-126">-WhatIf</span></span>
<span data-ttu-id="24635-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24635-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24635-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24635-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24635-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24635-129">CommonParameters</span></span>
<span data-ttu-id="24635-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24635-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24635-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24635-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24635-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24635-132">INPUTS</span></span>

### <span data-ttu-id="24635-133">System.String</span><span class="sxs-lookup"><span data-stu-id="24635-133">System.String</span></span>

## <span data-ttu-id="24635-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24635-134">OUTPUTS</span></span>

### <span data-ttu-id="24635-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24635-135">System.Boolean</span></span>

## <span data-ttu-id="24635-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="24635-136">NOTES</span></span>

## <span data-ttu-id="24635-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="24635-137">RELATED LINKS</span></span>

[<span data-ttu-id="24635-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24635-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="24635-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24635-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="24635-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24635-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


