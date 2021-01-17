---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304008"
---
# <span data-ttu-id="68ef4-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="68ef4-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="68ef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="68ef4-103">Aktualisiert die Vererbung der Aktualisierungskonfiguration für den Hauptzugriff auf die SCM-Website für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="68ef4-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="68ef4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68ef4-104">SYNTAX</span></span>

### <span data-ttu-id="68ef4-105">InputValuesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68ef4-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ef4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ef4-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ef4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68ef4-107">DESCRIPTION</span></span>
<span data-ttu-id="68ef4-108">Das **Cmdlet "Update-AzWebAppAccessRestrictionConfig"** aktualisiert die Zugriffseinschränkungskonfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="68ef4-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="68ef4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="68ef4-109">EXAMPLES</span></span>

### <span data-ttu-id="68ef4-110">Beispiel 1: Aktualisieren einer Web App-SCM-Website, um Zugriffseinschränkungen von der Hauptwebsite aus zu verwenden</span><span class="sxs-lookup"><span data-stu-id="68ef4-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="68ef4-111">Im folgenden Beispiel wird eine Web App mit dem Namen "IpRule" aktualisiert, die zur Ressourcengruppe "MyResourceGroup" gehört, um die Zugriffseinschränkungskonfiguration der Hauptwebsite auf der scm-Website zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="68ef4-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="68ef4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68ef4-112">PARAMETERS</span></span>

### <span data-ttu-id="68ef4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ef4-113">-DefaultProfile</span></span>
<span data-ttu-id="68ef4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68ef4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ef4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68ef4-115">-InputObject</span></span>
<span data-ttu-id="68ef4-116">Das Konfigurationsobjekt für Zugriffsbeschränkungen</span><span class="sxs-lookup"><span data-stu-id="68ef4-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ef4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="68ef4-117">-Name</span></span>
<span data-ttu-id="68ef4-118">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="68ef4-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ef4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68ef4-119">-PassThru</span></span>
<span data-ttu-id="68ef4-120">Geben Sie das Konfigurationsobjekt für Zugriffseinschränkungen zurück.</span><span class="sxs-lookup"><span data-stu-id="68ef4-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="68ef4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ef4-121">-ResourceGroupName</span></span>
<span data-ttu-id="68ef4-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="68ef4-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ef4-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="68ef4-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="68ef4-124">Die "Scm"-Website erbt Regeln, die auf der Hauptwebsite festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="68ef4-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ef4-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="68ef4-125">-SlotName</span></span>
<span data-ttu-id="68ef4-126">Name des Bereitstellungsplatzes.</span><span class="sxs-lookup"><span data-stu-id="68ef4-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ef4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68ef4-127">-Confirm</span></span>
<span data-ttu-id="68ef4-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68ef4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ef4-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="68ef4-129">-WhatIf</span></span>
<span data-ttu-id="68ef4-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68ef4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68ef4-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68ef4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ef4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ef4-132">CommonParameters</span></span>
<span data-ttu-id="68ef4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ef4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ef4-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68ef4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ef4-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="68ef4-135">INPUTS</span></span>

### <span data-ttu-id="68ef4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="68ef4-136">System.String</span></span>

### <span data-ttu-id="68ef4-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68ef4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68ef4-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="68ef4-138">OUTPUTS</span></span>

### <span data-ttu-id="68ef4-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="68ef4-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="68ef4-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="68ef4-140">NOTES</span></span>

## <span data-ttu-id="68ef4-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="68ef4-141">RELATED LINKS</span></span>

[<span data-ttu-id="68ef4-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="68ef4-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="68ef4-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="68ef4-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="68ef4-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="68ef4-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
