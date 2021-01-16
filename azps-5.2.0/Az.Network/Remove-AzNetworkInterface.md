---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294491"
---
# <span data-ttu-id="3a688-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3a688-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="3a688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a688-102">SYNOPSIS</span></span>
<span data-ttu-id="3a688-103">Entfernt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3a688-103">Removes a network interface.</span></span>

## <span data-ttu-id="3a688-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a688-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a688-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a688-105">DESCRIPTION</span></span>
<span data-ttu-id="3a688-106">Das **Cmdlet "Remove-AzNetworkInterface"** entfernt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3a688-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="3a688-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a688-107">EXAMPLES</span></span>

### <span data-ttu-id="3a688-108">Beispiel 1: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="3a688-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="3a688-109">Mit diesem Befehl wird die Netzwerkschnittstelle "NetworkInterface1" in der Ressourcengruppe "ResourceGroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a688-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="3a688-110">Da der *Parameter "Force"* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="3a688-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="3a688-111">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="3a688-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="3a688-112">Mit diesem Befehl werden alle Netzwerkschnittstellen in der Ressourcengruppe "ResourceGroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a688-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="3a688-113">Da der *Parameter "Force"* verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3a688-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="3a688-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a688-114">PARAMETERS</span></span>

### <span data-ttu-id="3a688-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a688-115">-AsJob</span></span>
<span data-ttu-id="3a688-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3a688-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a688-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a688-117">-DefaultProfile</span></span>
<span data-ttu-id="3a688-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a688-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a688-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3a688-119">-Force</span></span>
<span data-ttu-id="3a688-120">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="3a688-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a688-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a688-121">-Name</span></span>
<span data-ttu-id="3a688-122">Gibt den Namen der Netzwerkschnittstelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3a688-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a688-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a688-123">-PassThru</span></span>
<span data-ttu-id="3a688-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3a688-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a688-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3a688-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a688-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a688-126">-ResourceGroupName</span></span>
<span data-ttu-id="3a688-127">Gibt den Namen einer Ressourcengruppe an, die die netzwerkschnittstelle enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3a688-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a688-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a688-128">-Confirm</span></span>
<span data-ttu-id="3a688-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a688-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a688-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3a688-130">-WhatIf</span></span>
<span data-ttu-id="3a688-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a688-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a688-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a688-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a688-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a688-133">CommonParameters</span></span>
<span data-ttu-id="3a688-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a688-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a688-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a688-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a688-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a688-136">INPUTS</span></span>

### <span data-ttu-id="3a688-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3a688-137">System.String</span></span>

## <span data-ttu-id="3a688-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a688-138">OUTPUTS</span></span>

### <span data-ttu-id="3a688-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a688-139">System.Boolean</span></span>

## <span data-ttu-id="3a688-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a688-140">NOTES</span></span>

## <span data-ttu-id="3a688-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a688-141">RELATED LINKS</span></span>

[<span data-ttu-id="3a688-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3a688-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="3a688-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3a688-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="3a688-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3a688-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


