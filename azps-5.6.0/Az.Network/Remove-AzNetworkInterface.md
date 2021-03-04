---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940104"
---
# <span data-ttu-id="3de56-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3de56-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="3de56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de56-102">SYNOPSIS</span></span>
<span data-ttu-id="3de56-103">Entfernt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3de56-103">Removes a network interface.</span></span>

## <span data-ttu-id="3de56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3de56-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de56-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3de56-105">DESCRIPTION</span></span>
<span data-ttu-id="3de56-106">Das **Cmdlet Remove-AzNetworkInterface** entfernt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3de56-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="3de56-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3de56-107">EXAMPLES</span></span>

### <span data-ttu-id="3de56-108">Beispiel 1: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="3de56-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="3de56-109">Mit diesem Befehl wird die Netzwerkschnittstelle NetworkInterface1 in der Ressourcengruppe ResourceGroup1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="3de56-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="3de56-110">Da der *Parameter* Erzwingen nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="3de56-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="3de56-111">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="3de56-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="3de56-112">Mit diesem Befehl werden alle Netzwerkschnittstellen in der Ressourcengruppe ResourceGroup1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="3de56-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="3de56-113">Da der *Parameter* Erzwingen verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3de56-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="3de56-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3de56-114">PARAMETERS</span></span>

### <span data-ttu-id="3de56-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3de56-115">-AsJob</span></span>
<span data-ttu-id="3de56-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3de56-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3de56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de56-117">-DefaultProfile</span></span>
<span data-ttu-id="3de56-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3de56-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de56-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3de56-119">-Force</span></span>
<span data-ttu-id="3de56-120">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="3de56-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3de56-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3de56-121">-Name</span></span>
<span data-ttu-id="3de56-122">Gibt den Namen der Netzwerkschnittstelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3de56-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3de56-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3de56-123">-PassThru</span></span>
<span data-ttu-id="3de56-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3de56-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3de56-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3de56-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3de56-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de56-126">-ResourceGroupName</span></span>
<span data-ttu-id="3de56-127">Gibt den Namen einer Ressourcengruppe an, die die Netzwerkschnittstelle enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3de56-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3de56-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3de56-128">-Confirm</span></span>
<span data-ttu-id="3de56-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3de56-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de56-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de56-130">-WhatIf</span></span>
<span data-ttu-id="3de56-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3de56-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de56-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3de56-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de56-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de56-133">CommonParameters</span></span>
<span data-ttu-id="3de56-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de56-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de56-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de56-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de56-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3de56-136">INPUTS</span></span>

### <span data-ttu-id="3de56-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3de56-137">System.String</span></span>

## <span data-ttu-id="3de56-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3de56-138">OUTPUTS</span></span>

### <span data-ttu-id="3de56-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3de56-139">System.Boolean</span></span>

## <span data-ttu-id="3de56-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3de56-140">NOTES</span></span>

## <span data-ttu-id="3de56-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3de56-141">RELATED LINKS</span></span>

[<span data-ttu-id="3de56-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3de56-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="3de56-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3de56-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="3de56-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3de56-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


