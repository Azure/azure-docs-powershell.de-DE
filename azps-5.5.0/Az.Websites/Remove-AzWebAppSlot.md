---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174769"
---
# <span data-ttu-id="2e84f-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="2e84f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e84f-102">SYNOPSIS</span></span>

## <span data-ttu-id="2e84f-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e84f-103">SYNTAX</span></span>

### <span data-ttu-id="2e84f-104">S1</span><span class="sxs-lookup"><span data-stu-id="2e84f-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e84f-105">S2</span><span class="sxs-lookup"><span data-stu-id="2e84f-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e84f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e84f-106">DESCRIPTION</span></span>
<span data-ttu-id="2e84f-107">Das **Cmdlet "Remove-AzWebAppSlot"** entfernt ein Azure Web App-Slot, sofern die Ressourcengruppe und der Name der Web App angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2e84f-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="2e84f-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="2e84f-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="2e84f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e84f-109">EXAMPLES</span></span>

### <span data-ttu-id="2e84f-110">Beispiel 1: Entfernen eines Web -App-Slot</span><span class="sxs-lookup"><span data-stu-id="2e84f-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="2e84f-111">Mit diesem Befehl wird das Slot namens Slot001 entfernt, das der Web App ContosoSite zugeordnet ist und zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="2e84f-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2e84f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e84f-112">PARAMETERS</span></span>

### <span data-ttu-id="2e84f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e84f-113">-AsJob</span></span>
<span data-ttu-id="2e84f-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2e84f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e84f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e84f-115">-DefaultProfile</span></span>
<span data-ttu-id="2e84f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e84f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e84f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e84f-117">-Force</span></span>
<span data-ttu-id="2e84f-118">Option "Erzwingend entfernen"</span><span class="sxs-lookup"><span data-stu-id="2e84f-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2e84f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2e84f-119">-Name</span></span>
<span data-ttu-id="2e84f-120">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="2e84f-120">WebApp Name</span></span>

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

### <span data-ttu-id="2e84f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e84f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e84f-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2e84f-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2e84f-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="2e84f-123">-Slot</span></span>
<span data-ttu-id="2e84f-124">Name des WebApp-Slot</span><span class="sxs-lookup"><span data-stu-id="2e84f-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2e84f-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2e84f-125">-WebApp</span></span>
<span data-ttu-id="2e84f-126">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="2e84f-126">WebApp Object</span></span>

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

### <span data-ttu-id="2e84f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e84f-127">-Confirm</span></span>
<span data-ttu-id="2e84f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e84f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e84f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2e84f-129">-WhatIf</span></span>
<span data-ttu-id="2e84f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e84f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e84f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e84f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e84f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e84f-132">CommonParameters</span></span>
<span data-ttu-id="2e84f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e84f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e84f-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e84f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e84f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e84f-135">INPUTS</span></span>

### <span data-ttu-id="2e84f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2e84f-136">System.String</span></span>

### <span data-ttu-id="2e84f-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2e84f-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2e84f-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e84f-138">OUTPUTS</span></span>

### <span data-ttu-id="2e84f-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2e84f-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2e84f-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2e84f-140">NOTES</span></span>

## <span data-ttu-id="2e84f-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2e84f-141">RELATED LINKS</span></span>

[<span data-ttu-id="2e84f-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2e84f-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2e84f-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="2e84f-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="2e84f-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2e84f-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e84f-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2e84f-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e84f-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
