---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938416"
---
# <span data-ttu-id="7838a-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7838a-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="7838a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7838a-102">SYNOPSIS</span></span>
<span data-ttu-id="7838a-103">Entfernen Sie eine Routingregel aus dem Slot.</span><span class="sxs-lookup"><span data-stu-id="7838a-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="7838a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7838a-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7838a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7838a-105">DESCRIPTION</span></span>
<span data-ttu-id="7838a-106">Das **Cmdlet Remove-AzWebAppTrafficRouting** entfernt eine Routingregel aus einem Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="7838a-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="7838a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7838a-107">EXAMPLES</span></span>

### <span data-ttu-id="7838a-108">Beispiel 1 Entfernt die spezielle Routingregel aus dem Webapp-Slot</span><span class="sxs-lookup"><span data-stu-id="7838a-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="7838a-109">Mit diesem Befehl wird eine Routingregel für einen bestimmten WebApp-Slot entfernt.</span><span class="sxs-lookup"><span data-stu-id="7838a-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="7838a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7838a-110">PARAMETERS</span></span>

### <span data-ttu-id="7838a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7838a-111">-DefaultProfile</span></span>
<span data-ttu-id="7838a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7838a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7838a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7838a-113">-ResourceGroupName</span></span>
<span data-ttu-id="7838a-114">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7838a-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7838a-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7838a-115">-RuleName</span></span>
<span data-ttu-id="7838a-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="7838a-116">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7838a-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7838a-117">-WebAppName</span></span>
<span data-ttu-id="7838a-118">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="7838a-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7838a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7838a-119">-PassThru</span></span>
<span data-ttu-id="7838a-120">Geben Sie das Konfigurationsobjekt für Zugriffseinschränkungen zurück.</span><span class="sxs-lookup"><span data-stu-id="7838a-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="7838a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7838a-121">-Confirm</span></span>
<span data-ttu-id="7838a-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7838a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7838a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7838a-123">-WhatIf</span></span>
<span data-ttu-id="7838a-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7838a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7838a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7838a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7838a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7838a-126">CommonParameters</span></span>
<span data-ttu-id="7838a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7838a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7838a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7838a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7838a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7838a-129">INPUTS</span></span>

### <span data-ttu-id="7838a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="7838a-130">None</span></span>

## <span data-ttu-id="7838a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7838a-131">OUTPUTS</span></span>

### <span data-ttu-id="7838a-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="7838a-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="7838a-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7838a-133">NOTES</span></span>

## <span data-ttu-id="7838a-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7838a-134">RELATED LINKS</span></span>
[<span data-ttu-id="7838a-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7838a-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7838a-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7838a-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7838a-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7838a-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)