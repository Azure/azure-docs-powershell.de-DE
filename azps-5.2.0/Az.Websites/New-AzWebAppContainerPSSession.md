---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293729"
---
# <span data-ttu-id="831e1-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="831e1-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="831e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="831e1-102">SYNOPSIS</span></span>
<span data-ttu-id="831e1-103">New-AzWebAppContainerPSSession erstellt eine neue Remote-PowerShell-Sitzung im Windows-Container, der auf einer bestimmten Website oder einem bestimmten Slot und in einer bestimmten Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="831e1-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="831e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="831e1-104">SYNTAX</span></span>

### <span data-ttu-id="831e1-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="831e1-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="831e1-106">S2</span><span class="sxs-lookup"><span data-stu-id="831e1-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="831e1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="831e1-107">DESCRIPTION</span></span>
<span data-ttu-id="831e1-108">New-AzWebAppContainerPSSession erstellt eine neue Remote-PowerShell-Sitzung im Windows-Container, der auf einer bestimmten Website oder einem bestimmten Slot und in einer bestimmten Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="831e1-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="831e1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="831e1-109">EXAMPLES</span></span>

### <span data-ttu-id="831e1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="831e1-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="831e1-111">Dadurch wird eine neue Remote-PowerShell-Sitzung in der Windows-Container-App ContosoASP erstellt und die Prozesse angezeigt, die im Container "ContosoASP" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="831e1-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="831e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="831e1-112">PARAMETERS</span></span>

### <span data-ttu-id="831e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831e1-113">-DefaultProfile</span></span>
<span data-ttu-id="831e1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="831e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="831e1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="831e1-115">-Force</span></span>
<span data-ttu-id="831e1-116">Erstellen Sie die PowerShell-Sitzung, ohne zur Bestätigung zu aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="831e1-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="831e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="831e1-117">-Name</span></span>
<span data-ttu-id="831e1-118">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="831e1-118">The name of the web app.</span></span>

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

### <span data-ttu-id="831e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="831e1-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="831e1-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="831e1-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="831e1-121">-SlotName</span></span>
<span data-ttu-id="831e1-122">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="831e1-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="831e1-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="831e1-123">-WebApp</span></span>
<span data-ttu-id="831e1-124">Web -App-Objekt</span><span class="sxs-lookup"><span data-stu-id="831e1-124">The web app object</span></span>

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

### <span data-ttu-id="831e1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="831e1-125">-Confirm</span></span>
<span data-ttu-id="831e1-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="831e1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="831e1-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="831e1-127">-WhatIf</span></span>
<span data-ttu-id="831e1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="831e1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="831e1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="831e1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="831e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831e1-130">CommonParameters</span></span>
<span data-ttu-id="831e1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831e1-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="831e1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831e1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="831e1-133">INPUTS</span></span>

### <span data-ttu-id="831e1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="831e1-134">System.String</span></span>

### <span data-ttu-id="831e1-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="831e1-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="831e1-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="831e1-136">OUTPUTS</span></span>

### <span data-ttu-id="831e1-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="831e1-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="831e1-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="831e1-138">NOTES</span></span>

## <span data-ttu-id="831e1-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="831e1-139">RELATED LINKS</span></span>
