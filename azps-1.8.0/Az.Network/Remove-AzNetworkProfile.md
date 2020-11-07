---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: ac34f2d8c2a48010792716f183a6b86cce714294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660349"
---
# <span data-ttu-id="3ca0d-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="3ca0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ca0d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca0d-103">Entfernt ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-103">Removes a network profile.</span></span>

## <span data-ttu-id="3ca0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ca0d-104">SYNTAX</span></span>

### <span data-ttu-id="3ca0d-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ca0d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca0d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca0d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca0d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ca0d-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca0d-109">Das Cmdlet **Remove-AzNetworkProfile** entfernt ein Netzwerkprofil, wenn keine Container Netzwerkschnittstellen (im Gegensatz zu einer Container-Netzwerkschnittstellen **Konfiguration** ) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="3ca0d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ca0d-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca0d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ca0d-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="3ca0d-112">Dadurch wird das Netzwerkprofil mit dem Namen Np1 aus der Ressourcengruppe RG1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="3ca0d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ca0d-113">PARAMETERS</span></span>

### <span data-ttu-id="3ca0d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ca0d-114">-AsJob</span></span>
<span data-ttu-id="3ca0d-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3ca0d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ca0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-116">-DefaultProfile</span></span>
<span data-ttu-id="3ca0d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca0d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3ca0d-118">-Force</span></span>
<span data-ttu-id="3ca0d-119">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="3ca0d-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3ca0d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ca0d-120">-InputObject</span></span>
<span data-ttu-id="3ca0d-121">Netzwerkprofil Objekt.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-121">Network profile object.</span></span>

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

### <span data-ttu-id="3ca0d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3ca0d-122">-Name</span></span>
<span data-ttu-id="3ca0d-123">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="3ca0d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ca0d-124">-PassThru</span></span>
<span data-ttu-id="3ca0d-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="3ca0d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca0d-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ca0d-127">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="3ca0d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3ca0d-128">-ResourceId</span></span>
<span data-ttu-id="3ca0d-129">Die Azure Resource Manager-Ressourcen-ID des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="3ca0d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ca0d-130">-Confirm</span></span>
<span data-ttu-id="3ca0d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca0d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca0d-132">-WhatIf</span></span>
<span data-ttu-id="3ca0d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca0d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca0d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca0d-135">CommonParameters</span></span>
<span data-ttu-id="3ca0d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca0d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca0d-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca0d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca0d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ca0d-138">INPUTS</span></span>

### <span data-ttu-id="3ca0d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca0d-139">System.String</span></span>

### <span data-ttu-id="3ca0d-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="3ca0d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ca0d-141">OUTPUTS</span></span>

### <span data-ttu-id="3ca0d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ca0d-142">System.Boolean</span></span>

## <span data-ttu-id="3ca0d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ca0d-143">NOTES</span></span>

## <span data-ttu-id="3ca0d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ca0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="3ca0d-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="3ca0d-146">Neu – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="3ca0d-147">Satz-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0d-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
