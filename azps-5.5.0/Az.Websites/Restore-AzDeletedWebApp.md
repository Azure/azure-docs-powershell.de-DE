---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162692"
---
# <span data-ttu-id="174b5-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="174b5-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="174b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="174b5-102">SYNOPSIS</span></span>
<span data-ttu-id="174b5-103">Stellt eine gelöschte Web App in einer neuen oder vorhandenen Web App wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="174b5-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="174b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="174b5-104">SYNTAX</span></span>

### <span data-ttu-id="174b5-105">FromDeletedResourceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="174b5-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="174b5-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="174b5-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="174b5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="174b5-107">DESCRIPTION</span></span>
<span data-ttu-id="174b5-108">Mit **dem Cmdlet "Restore-AzDeletedWebApp"** wird eine gelöschte Web App wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="174b5-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="174b5-109">Die durch TargetResourceGroupName, TargetName und TargetSlot angegebene Web App wird mit den Inhalten und Einstellungen der gelöschten Web App überschrieben.</span><span class="sxs-lookup"><span data-stu-id="174b5-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="174b5-110">Wenn die Zielparameter nicht angegeben werden, werden sie automatisch mit der Ressourcengruppe, dem Namen und dem Platz der gelöschten Web App ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="174b5-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="174b5-111">Wenn die Ziel-Web-App nicht vorhanden ist, wird sie automatisch in dem von TargetAppServicePlanName angegebenen App-Dienstplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="174b5-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="174b5-112">Der Parameter "RestoreContentOnly" kann verwendet werden, um nur die Dateien der gelöschten App ohne die Einstellungen der App wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="174b5-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="174b5-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="174b5-113">EXAMPLES</span></span>

### <span data-ttu-id="174b5-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="174b5-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="174b5-115">Stellt eine gelöschte App namens "ContosoApp" wieder dar, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="174b5-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="174b5-116">Im App-Serviceplan mit dem Namen "ContosoPlan" wird eine neue App mit demselben Namen und derselben Ressourcengruppe erstellt, und die Dateien und Einstellungen der gelöschten App werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="174b5-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="174b5-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="174b5-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="174b5-118">Stellt den Stagingplatz einer gelöschten App namens "ContosoApp" wieder dar, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="174b5-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="174b5-119">Die Zur Ressourcengruppe "Default-Web-EastUS" gehörende Web-App namens "ContosoRestore" wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="174b5-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="174b5-120">Die gelöschten Web -App-Einstellungen werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="174b5-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="174b5-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="174b5-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="174b5-122">Falls es zwei gelöschte Apps mit demselben Namen (ContosoApp) gibt, erhalten wir Details zu beiden Websites und stellen die App mit der App Ihrer Wahl wieder zusammen, indem wir die Wiederherstellung mit ID aufrufen.</span><span class="sxs-lookup"><span data-stu-id="174b5-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="174b5-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="174b5-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="174b5-124">Falls zwei gelöschte Apps mit demselben Namen (ContosoApp) vorhanden sind, erhalten wir Details zu beiden Websites und stellen die App mit der App Ihrer Wahl wieder her, indem wir die Wiederherstellung mit InputObject(Deletedsite)-Details aufrufen.</span><span class="sxs-lookup"><span data-stu-id="174b5-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="174b5-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="174b5-125">PARAMETERS</span></span>

### <span data-ttu-id="174b5-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="174b5-126">-AsJob</span></span>
<span data-ttu-id="174b5-127">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="174b5-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="174b5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174b5-128">-DefaultProfile</span></span>
<span data-ttu-id="174b5-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="174b5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="174b5-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="174b5-130">-DeletedId</span></span>
<span data-ttu-id="174b5-131">Die ID der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-131">The Id of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-132">-Force</span><span class="sxs-lookup"><span data-stu-id="174b5-132">-Force</span></span>
<span data-ttu-id="174b5-133">Stellen Sie die Wiederherstellung ohne Bestätigungsaufforderung vor.</span><span class="sxs-lookup"><span data-stu-id="174b5-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="174b5-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="174b5-134">-InputObject</span></span>
<span data-ttu-id="174b5-135">Die gelöschte Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-135">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-136">-Location</span><span class="sxs-lookup"><span data-stu-id="174b5-136">-Location</span></span>
<span data-ttu-id="174b5-137">Der Speicherort der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-137">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-138">-Name</span><span class="sxs-lookup"><span data-stu-id="174b5-138">-Name</span></span>
<span data-ttu-id="174b5-139">Der Name der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-139">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174b5-140">-ResourceGroupName</span></span>
<span data-ttu-id="174b5-141">Die Ressourcengruppe der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-141">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="174b5-142">-RestoreContentOnly</span></span>
<span data-ttu-id="174b5-143">Wiederherstellen der Web-App-Dateien, aber nicht Wiederherstellen der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="174b5-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="174b5-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="174b5-144">-Slot</span></span>
<span data-ttu-id="174b5-145">Der gelöschte Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="174b5-145">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="174b5-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="174b5-147">Der App-Dienstplan für die neue Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-147">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="174b5-148">-TargetName</span></span>
<span data-ttu-id="174b5-149">Der Name der neuen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="174b5-149">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174b5-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="174b5-151">Die Ressourcengruppe, die die neue Azure Web App enthält.</span><span class="sxs-lookup"><span data-stu-id="174b5-151">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="174b5-152">-TargetSlot</span></span>
<span data-ttu-id="174b5-153">Der Name des neuen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="174b5-153">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174b5-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="174b5-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="174b5-155">Zum Wiederherstellen einer gelöschten App aus einer Skalierungseinheit, die offline ist.</span><span class="sxs-lookup"><span data-stu-id="174b5-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="174b5-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="174b5-156">-Confirm</span></span>
<span data-ttu-id="174b5-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="174b5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="174b5-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="174b5-158">-WhatIf</span></span>
<span data-ttu-id="174b5-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="174b5-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="174b5-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="174b5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="174b5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174b5-161">CommonParameters</span></span>
<span data-ttu-id="174b5-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174b5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174b5-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174b5-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174b5-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="174b5-164">INPUTS</span></span>

### <span data-ttu-id="174b5-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="174b5-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="174b5-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="174b5-166">OUTPUTS</span></span>

### <span data-ttu-id="174b5-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="174b5-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="174b5-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="174b5-168">NOTES</span></span>

## <span data-ttu-id="174b5-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="174b5-169">RELATED LINKS</span></span>

[<span data-ttu-id="174b5-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="174b5-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)