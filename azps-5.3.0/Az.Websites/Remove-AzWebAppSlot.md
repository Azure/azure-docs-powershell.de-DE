---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460367"
---
# <span data-ttu-id="45579-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="45579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45579-102">SYNOPSIS</span></span>

## <span data-ttu-id="45579-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45579-103">SYNTAX</span></span>

### <span data-ttu-id="45579-104">S1</span><span class="sxs-lookup"><span data-stu-id="45579-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45579-105">S2</span><span class="sxs-lookup"><span data-stu-id="45579-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45579-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45579-106">DESCRIPTION</span></span>
<span data-ttu-id="45579-107">Das **Cmdlet "Remove-AzWebAppSlot"** entfernt ein Azure Web App-Slot, sofern die Ressourcengruppe und der Name der Web App angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="45579-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="45579-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="45579-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="45579-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45579-109">EXAMPLES</span></span>

### <span data-ttu-id="45579-110">Beispiel 1: Entfernen eines Web -App-Slot</span><span class="sxs-lookup"><span data-stu-id="45579-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="45579-111">Mit diesem Befehl wird das Slot namens Slot001 entfernt, das der Web App ContosoSite zugeordnet ist und zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="45579-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="45579-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45579-112">PARAMETERS</span></span>

### <span data-ttu-id="45579-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45579-113">-AsJob</span></span>
<span data-ttu-id="45579-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="45579-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45579-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45579-115">-DefaultProfile</span></span>
<span data-ttu-id="45579-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45579-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45579-117">-Force</span><span class="sxs-lookup"><span data-stu-id="45579-117">-Force</span></span>
<span data-ttu-id="45579-118">Option "Erzwingend entfernen"</span><span class="sxs-lookup"><span data-stu-id="45579-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="45579-119">-Name</span><span class="sxs-lookup"><span data-stu-id="45579-119">-Name</span></span>
<span data-ttu-id="45579-120">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="45579-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45579-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45579-121">-ResourceGroupName</span></span>
<span data-ttu-id="45579-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="45579-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45579-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="45579-123">-Slot</span></span>
<span data-ttu-id="45579-124">Name des WebApp-Slot</span><span class="sxs-lookup"><span data-stu-id="45579-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45579-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="45579-125">-WebApp</span></span>
<span data-ttu-id="45579-126">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="45579-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45579-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45579-127">-Confirm</span></span>
<span data-ttu-id="45579-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45579-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45579-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="45579-129">-WhatIf</span></span>
<span data-ttu-id="45579-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45579-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45579-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45579-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45579-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45579-132">CommonParameters</span></span>
<span data-ttu-id="45579-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45579-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45579-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45579-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45579-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45579-135">INPUTS</span></span>

### <span data-ttu-id="45579-136">System.String</span><span class="sxs-lookup"><span data-stu-id="45579-136">System.String</span></span>

### <span data-ttu-id="45579-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="45579-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="45579-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45579-138">OUTPUTS</span></span>

### <span data-ttu-id="45579-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="45579-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="45579-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45579-140">NOTES</span></span>

## <span data-ttu-id="45579-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45579-141">RELATED LINKS</span></span>

[<span data-ttu-id="45579-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="45579-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="45579-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="45579-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="45579-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="45579-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45579-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="45579-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="45579-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
