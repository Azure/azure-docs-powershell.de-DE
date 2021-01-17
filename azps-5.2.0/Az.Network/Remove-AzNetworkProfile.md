---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370949"
---
# <span data-ttu-id="31a3c-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a3c-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="31a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="31a3c-103">Entfernt ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="31a3c-103">Removes a network profile.</span></span>

## <span data-ttu-id="31a3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31a3c-104">SYNTAX</span></span>

### <span data-ttu-id="31a3c-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="31a3c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a3c-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31a3c-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a3c-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31a3c-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a3c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31a3c-108">DESCRIPTION</span></span>
<span data-ttu-id="31a3c-109">Das **Cmdlet "Remove-AzNetworkProfile"** entfernt ein Netzwerkprofil, wenn keine Containernetzwerkschnittstellen (im Gegensatz zu einer Containerkonfiguration der Netzwerkschnittstelle) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="31a3c-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="31a3c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31a3c-110">EXAMPLES</span></span>

### <span data-ttu-id="31a3c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="31a3c-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="31a3c-112">Dadurch wird das Netzwerkprofil mit dem Namen np1 aus der Ressourcengruppe "rg1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="31a3c-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="31a3c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31a3c-113">PARAMETERS</span></span>

### <span data-ttu-id="31a3c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31a3c-114">-AsJob</span></span>
<span data-ttu-id="31a3c-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="31a3c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31a3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a3c-116">-DefaultProfile</span></span>
<span data-ttu-id="31a3c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31a3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a3c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="31a3c-118">-Force</span></span>
<span data-ttu-id="31a3c-119">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="31a3c-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="31a3c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31a3c-120">-InputObject</span></span>
<span data-ttu-id="31a3c-121">Netzwerkprofilobjekt.</span><span class="sxs-lookup"><span data-stu-id="31a3c-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31a3c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="31a3c-122">-Name</span></span>
<span data-ttu-id="31a3c-123">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="31a3c-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a3c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31a3c-124">-PassThru</span></span>
<span data-ttu-id="31a3c-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="31a3c-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="31a3c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a3c-126">-ResourceGroupName</span></span>
<span data-ttu-id="31a3c-127">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="31a3c-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a3c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31a3c-128">-ResourceId</span></span>
<span data-ttu-id="31a3c-129">Die Ressourcen-ID des Azure-Ressourcen-Managers im Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="31a3c-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a3c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31a3c-130">-Confirm</span></span>
<span data-ttu-id="31a3c-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31a3c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a3c-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="31a3c-132">-WhatIf</span></span>
<span data-ttu-id="31a3c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31a3c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a3c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31a3c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a3c-135">CommonParameters</span></span>
<span data-ttu-id="31a3c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a3c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a3c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a3c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31a3c-138">INPUTS</span></span>

### <span data-ttu-id="31a3c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="31a3c-139">System.String</span></span>

### <span data-ttu-id="31a3c-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a3c-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="31a3c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31a3c-141">OUTPUTS</span></span>

### <span data-ttu-id="31a3c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31a3c-142">System.Boolean</span></span>

## <span data-ttu-id="31a3c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="31a3c-143">NOTES</span></span>

## <span data-ttu-id="31a3c-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="31a3c-144">RELATED LINKS</span></span>

[<span data-ttu-id="31a3c-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a3c-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="31a3c-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a3c-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="31a3c-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a3c-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
