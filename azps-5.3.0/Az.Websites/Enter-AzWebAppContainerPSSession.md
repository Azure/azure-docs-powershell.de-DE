---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460476"
---
# <span data-ttu-id="c3e14-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="c3e14-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="c3e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e14-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e14-103">Öffnet eine Remote-PowerShell-Sitzung in dem Windows-Container, der auf einer bestimmten Website oder einem bestimmten Slot und in einer bestimmten Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3e14-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="c3e14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3e14-104">SYNTAX</span></span>

### <span data-ttu-id="c3e14-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3e14-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e14-106">S2</span><span class="sxs-lookup"><span data-stu-id="c3e14-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e14-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3e14-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e14-108">öffnet eine Remote-PowerShell-Sitzung in dem Windows-Container, der auf einer bestimmten Website oder einem bestimmten Slot und in einer bestimmten Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3e14-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="c3e14-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3e14-109">EXAMPLES</span></span>

### <span data-ttu-id="c3e14-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3e14-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="c3e14-111">Mit diesem Befehl wird eine Remote-PowerShell-Sitzung in der Windows-Container-App ContosoASP geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c3e14-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="c3e14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3e14-112">PARAMETERS</span></span>

### <span data-ttu-id="c3e14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e14-113">-DefaultProfile</span></span>
<span data-ttu-id="c3e14-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3e14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e14-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3e14-115">-Force</span></span>
<span data-ttu-id="c3e14-116">Erstellen Sie die PowerShell-Sitzung, ohne zur Bestätigung zu aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="c3e14-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c3e14-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c3e14-117">-Name</span></span>
<span data-ttu-id="c3e14-118">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="c3e14-118">The name of the web app.</span></span>

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

### <span data-ttu-id="c3e14-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3e14-119">-PassThru</span></span>
<span data-ttu-id="c3e14-120">Zurückgeben eines Werts, der Erfolg oder Misserfolg angibt</span><span class="sxs-lookup"><span data-stu-id="c3e14-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="c3e14-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e14-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3e14-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3e14-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3e14-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="c3e14-123">-SlotName</span></span>
<span data-ttu-id="c3e14-124">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="c3e14-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e14-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c3e14-125">-WebApp</span></span>
<span data-ttu-id="c3e14-126">Web -App-Objekt</span><span class="sxs-lookup"><span data-stu-id="c3e14-126">The web app object</span></span>

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

### <span data-ttu-id="c3e14-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3e14-127">-Confirm</span></span>
<span data-ttu-id="c3e14-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3e14-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e14-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c3e14-129">-WhatIf</span></span>
<span data-ttu-id="c3e14-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e14-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3e14-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3e14-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e14-132">CommonParameters</span></span>
<span data-ttu-id="c3e14-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e14-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e14-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e14-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3e14-135">INPUTS</span></span>

### <span data-ttu-id="c3e14-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e14-136">System.String</span></span>

### <span data-ttu-id="c3e14-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c3e14-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c3e14-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3e14-138">OUTPUTS</span></span>

### <span data-ttu-id="c3e14-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="c3e14-139">System.Void</span></span>

## <span data-ttu-id="c3e14-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c3e14-140">NOTES</span></span>

## <span data-ttu-id="c3e14-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c3e14-141">RELATED LINKS</span></span>
