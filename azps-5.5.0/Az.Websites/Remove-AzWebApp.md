---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149676"
---
# <span data-ttu-id="50a58-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="50a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a58-102">SYNOPSIS</span></span>
<span data-ttu-id="50a58-103">Entfernt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="50a58-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="50a58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50a58-104">SYNTAX</span></span>

### <span data-ttu-id="50a58-105">S1</span><span class="sxs-lookup"><span data-stu-id="50a58-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a58-106">S2</span><span class="sxs-lookup"><span data-stu-id="50a58-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a58-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50a58-107">DESCRIPTION</span></span>
<span data-ttu-id="50a58-108">Mit **dem Cmdlet "Remove-AzWebApp"** wird eine Azure Web App entfernt, für die die Ressourcengruppe und der Name der Web App angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="50a58-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="50a58-109">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="50a58-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="50a58-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50a58-110">EXAMPLES</span></span>

### <span data-ttu-id="50a58-111">Beispiel 1: Entfernen einer Web App</span><span class="sxs-lookup"><span data-stu-id="50a58-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="50a58-112">Mit diesem Befehl wird die Azure Web App namens "ContosoSite" entfernt, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="50a58-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="50a58-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50a58-113">PARAMETERS</span></span>

### <span data-ttu-id="50a58-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50a58-114">-AsJob</span></span>
<span data-ttu-id="50a58-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="50a58-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50a58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a58-116">-DefaultProfile</span></span>
<span data-ttu-id="50a58-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50a58-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50a58-118">-Force</span><span class="sxs-lookup"><span data-stu-id="50a58-118">-Force</span></span>
<span data-ttu-id="50a58-119">Option "Erzwingend entfernen"</span><span class="sxs-lookup"><span data-stu-id="50a58-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="50a58-120">-Name</span><span class="sxs-lookup"><span data-stu-id="50a58-120">-Name</span></span>
<span data-ttu-id="50a58-121">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="50a58-121">WebApp Name</span></span>

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

### <span data-ttu-id="50a58-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a58-122">-ResourceGroupName</span></span>
<span data-ttu-id="50a58-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="50a58-123">Resource Group Name</span></span>

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

### <span data-ttu-id="50a58-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-124">-WebApp</span></span>
<span data-ttu-id="50a58-125">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="50a58-125">WebApp Object</span></span>

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

### <span data-ttu-id="50a58-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50a58-126">-Confirm</span></span>
<span data-ttu-id="50a58-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen. Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50a58-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a58-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50a58-128">-WhatIf</span></span>
<span data-ttu-id="50a58-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50a58-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a58-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50a58-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a58-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50a58-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a58-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a58-132">CommonParameters</span></span>
<span data-ttu-id="50a58-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a58-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a58-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a58-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a58-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50a58-135">INPUTS</span></span>

### <span data-ttu-id="50a58-136">System.String</span><span class="sxs-lookup"><span data-stu-id="50a58-136">System.String</span></span>

### <span data-ttu-id="50a58-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="50a58-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="50a58-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50a58-138">OUTPUTS</span></span>

### <span data-ttu-id="50a58-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="50a58-139">System.Void</span></span>

## <span data-ttu-id="50a58-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50a58-140">NOTES</span></span>

## <span data-ttu-id="50a58-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50a58-141">RELATED LINKS</span></span>

[<span data-ttu-id="50a58-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="50a58-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="50a58-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="50a58-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="50a58-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50a58-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


