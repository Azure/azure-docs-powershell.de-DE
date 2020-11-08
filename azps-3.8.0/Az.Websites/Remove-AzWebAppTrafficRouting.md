---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003124"
---
# <span data-ttu-id="2f51f-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2f51f-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="2f51f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f51f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f51f-103">Entfernen Sie eine Routingregel aus dem Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="2f51f-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="2f51f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f51f-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f51f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f51f-105">DESCRIPTION</span></span>
<span data-ttu-id="2f51f-106">Das Cmdlet **Remove-AzWebAppTrafficRouting** entfernt eine Routingregel aus einem Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="2f51f-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="2f51f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f51f-107">EXAMPLES</span></span>

### <span data-ttu-id="2f51f-108">Beispiel 1 entfernt die spezifische Routingregel aus dem Webablage-Steckplatz</span><span class="sxs-lookup"><span data-stu-id="2f51f-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="2f51f-109">Mit diesem Befehl wird eine Routingregel für einen bestimmten webaktions Steckplatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="2f51f-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="2f51f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f51f-110">PARAMETERS</span></span>

### <span data-ttu-id="2f51f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f51f-111">-DefaultProfile</span></span>
<span data-ttu-id="2f51f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f51f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f51f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f51f-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f51f-114">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2f51f-114">Resource Group Name</span></span>

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

### <span data-ttu-id="2f51f-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="2f51f-115">-RuleName</span></span>
<span data-ttu-id="2f51f-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="2f51f-116">Rule Name</span></span>

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

### <span data-ttu-id="2f51f-117">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="2f51f-117">-WebAppName</span></span>
<span data-ttu-id="2f51f-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="2f51f-118">WebApp Name</span></span>

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

### <span data-ttu-id="2f51f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f51f-119">-PassThru</span></span>
<span data-ttu-id="2f51f-120">Gibt das Config-Objekt für die Zugriffsbeschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="2f51f-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="2f51f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f51f-121">-Confirm</span></span>
<span data-ttu-id="2f51f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f51f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f51f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f51f-123">-WhatIf</span></span>
<span data-ttu-id="2f51f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f51f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f51f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f51f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f51f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f51f-126">CommonParameters</span></span>
<span data-ttu-id="2f51f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f51f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f51f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f51f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f51f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f51f-129">INPUTS</span></span>

### <span data-ttu-id="2f51f-130">Keine</span><span class="sxs-lookup"><span data-stu-id="2f51f-130">None</span></span>

## <span data-ttu-id="2f51f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f51f-131">OUTPUTS</span></span>

### <span data-ttu-id="2f51f-132">Microsoft. Azure. Management. Websites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="2f51f-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="2f51f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f51f-133">NOTES</span></span>

## <span data-ttu-id="2f51f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f51f-134">RELATED LINKS</span></span>
[<span data-ttu-id="2f51f-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2f51f-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="2f51f-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2f51f-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="2f51f-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2f51f-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)