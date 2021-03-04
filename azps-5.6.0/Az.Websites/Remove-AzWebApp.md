---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923147"
---
# <span data-ttu-id="d000d-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="d000d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d000d-102">SYNOPSIS</span></span>
<span data-ttu-id="d000d-103">Entfernt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d000d-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="d000d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d000d-104">SYNTAX</span></span>

### <span data-ttu-id="d000d-105">S1</span><span class="sxs-lookup"><span data-stu-id="d000d-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d000d-106">S2</span><span class="sxs-lookup"><span data-stu-id="d000d-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d000d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d000d-107">DESCRIPTION</span></span>
<span data-ttu-id="d000d-108">Das **Cmdlet Remove-AzWebApp** entfernt eine Azure Web App, die die Ressourcengruppe und den Web App-Namen bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="d000d-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="d000d-109">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="d000d-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d000d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d000d-110">EXAMPLES</span></span>

### <span data-ttu-id="d000d-111">Beispiel 1: Entfernen einer Web App</span><span class="sxs-lookup"><span data-stu-id="d000d-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d000d-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite entfernt, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="d000d-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d000d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d000d-113">PARAMETERS</span></span>

### <span data-ttu-id="d000d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d000d-114">-AsJob</span></span>
<span data-ttu-id="d000d-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d000d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d000d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d000d-116">-DefaultProfile</span></span>
<span data-ttu-id="d000d-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d000d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d000d-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d000d-118">-Force</span></span>
<span data-ttu-id="d000d-119">Option "Mit Gewalt entfernen"</span><span class="sxs-lookup"><span data-stu-id="d000d-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d000d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d000d-120">-Name</span></span>
<span data-ttu-id="d000d-121">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="d000d-121">WebApp Name</span></span>

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

### <span data-ttu-id="d000d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d000d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d000d-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d000d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d000d-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-124">-WebApp</span></span>
<span data-ttu-id="d000d-125">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="d000d-125">WebApp Object</span></span>

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

### <span data-ttu-id="d000d-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d000d-126">-Confirm</span></span>
<span data-ttu-id="d000d-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen. Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d000d-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d000d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d000d-128">-WhatIf</span></span>
<span data-ttu-id="d000d-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d000d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d000d-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d000d-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d000d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d000d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d000d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d000d-132">CommonParameters</span></span>
<span data-ttu-id="d000d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d000d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d000d-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d000d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d000d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d000d-135">INPUTS</span></span>

### <span data-ttu-id="d000d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d000d-136">System.String</span></span>

### <span data-ttu-id="d000d-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d000d-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d000d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d000d-138">OUTPUTS</span></span>

### <span data-ttu-id="d000d-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="d000d-139">System.Void</span></span>

## <span data-ttu-id="d000d-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d000d-140">NOTES</span></span>

## <span data-ttu-id="d000d-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d000d-141">RELATED LINKS</span></span>

[<span data-ttu-id="d000d-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d000d-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d000d-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d000d-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d000d-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d000d-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


