---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482222"
---
# <span data-ttu-id="046d8-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="046d8-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="046d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="046d8-102">SYNOPSIS</span></span>
<span data-ttu-id="046d8-103">Entfernt einen virtuellen Netzwerk-Tap.</span><span class="sxs-lookup"><span data-stu-id="046d8-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="046d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="046d8-104">SYNTAX</span></span>

### <span data-ttu-id="046d8-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="046d8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046d8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="046d8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046d8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="046d8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="046d8-108">DESCRIPTION</span></span>
<span data-ttu-id="046d8-109">Das Cmdlet " **Remove-AzureRmVirtualNetworkTap** " entfernt einen virtuellen Azure-Netzwerk-Tap.</span><span class="sxs-lookup"><span data-stu-id="046d8-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="046d8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="046d8-110">EXAMPLES</span></span>

### <span data-ttu-id="046d8-111">Beispiel 1: Entfernen eines virtuak-Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="046d8-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="046d8-112">Dieser Befehl entfernt die VirtualNetworkTap1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="046d8-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="046d8-113">Da der Parameter *Force* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="046d8-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="046d8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="046d8-114">PARAMETERS</span></span>

### <span data-ttu-id="046d8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="046d8-115">-AsJob</span></span>
<span data-ttu-id="046d8-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="046d8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="046d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046d8-117">-DefaultProfile</span></span>
<span data-ttu-id="046d8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="046d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="046d8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="046d8-119">-Force</span></span>
<span data-ttu-id="046d8-120">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="046d8-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="046d8-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="046d8-121">-InputObject</span></span>
<span data-ttu-id="046d8-122">Bezug auf die VirtualNetworkTap-Ressource</span><span class="sxs-lookup"><span data-stu-id="046d8-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="046d8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="046d8-123">-Name</span></span>
<span data-ttu-id="046d8-124">Der Name des Tap.</span><span class="sxs-lookup"><span data-stu-id="046d8-124">The name of the tap.</span></span>

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

### <span data-ttu-id="046d8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="046d8-125">-PassThru</span></span>
<span data-ttu-id="046d8-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="046d8-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="046d8-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="046d8-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="046d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="046d8-129">Der Ressourcengruppenname des virtuellen Netzwerks Tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="046d8-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="046d8-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="046d8-130">-ResourceId</span></span>
<span data-ttu-id="046d8-131">VirtualNetworkTap-Quell Code</span><span class="sxs-lookup"><span data-stu-id="046d8-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046d8-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="046d8-132">-Confirm</span></span>
<span data-ttu-id="046d8-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="046d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046d8-134">-WhatIf</span></span>
<span data-ttu-id="046d8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="046d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046d8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="046d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046d8-137">CommonParameters</span></span>
<span data-ttu-id="046d8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046d8-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046d8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046d8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="046d8-140">INPUTS</span></span>

### <span data-ttu-id="046d8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="046d8-141">System.String</span></span>

## <span data-ttu-id="046d8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="046d8-142">OUTPUTS</span></span>

### <span data-ttu-id="046d8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="046d8-143">System.Boolean</span></span>

## <span data-ttu-id="046d8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="046d8-144">NOTES</span></span>

## <span data-ttu-id="046d8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="046d8-145">RELATED LINKS</span></span>
