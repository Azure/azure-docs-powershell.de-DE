---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167140"
---
# <span data-ttu-id="5d187-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5d187-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="5d187-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d187-102">SYNOPSIS</span></span>
<span data-ttu-id="5d187-103">Stellt eine gelöschte Web-App in einer neuen oder vorhandenen Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="5d187-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="5d187-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d187-104">SYNTAX</span></span>

### <span data-ttu-id="5d187-105">FromDeletedResourceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d187-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d187-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="5d187-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d187-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d187-107">DESCRIPTION</span></span>
<span data-ttu-id="5d187-108">Das Cmdlet **Restore-AzDeletedWebApp** stellt eine gelöschte Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="5d187-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="5d187-109">Die von TargetResourceGroupName, TargetName und TargetSlot angegebene Web-App wird mit den Inhalten und Einstellungen der gelöschten Web-App überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5d187-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="5d187-110">Wenn die Zielparameter nicht angegeben werden, werden Sie automatisch mit der Ressourcengruppe, dem Namen und dem Slot der gelöschten Web App gefüllt.</span><span class="sxs-lookup"><span data-stu-id="5d187-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="5d187-111">Wenn die Ziel-Web-App nicht vorhanden ist, wird Sie automatisch im App-Service Plan erstellt, der von TargetAppServicePlanName angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d187-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="5d187-112">Der RestoreContentOnly-Parameter kann verwendet werden, um nur die gelöschten APP-Dateien ohne die App-Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="5d187-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="5d187-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d187-113">EXAMPLES</span></span>

### <span data-ttu-id="5d187-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d187-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="5d187-115">Stellt eine gelöschte App mit dem Namen ContosoApp wieder her, die zur Ressourcengruppe Standard-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="5d187-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="5d187-116">Eine neue APP mit dem gleichen Namen und der gleichen Ressourcengruppe wird im App-Service Plan mit dem Namen ContosoPlan erstellt, und die Dateien und Einstellungen der gelöschten App werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5d187-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="5d187-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d187-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="5d187-118">Stellt den Staging-Slot einer gelöschten App mit dem Namen ContosoApp wieder her, die zur Ressourcengruppe Standard-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="5d187-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="5d187-119">Die Web-App mit dem Namen ContosoRestore, die zum Standard-Web-eastus der Ressourcengruppe gehört, wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5d187-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="5d187-120">Die Einstellungen für gelöschte Web App werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5d187-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="5d187-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5d187-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="5d187-122">Wenn zwei gelöschte apps mit dem gleichen Namen (ContosoApp) vorhanden sind, erhalten Sie Details zu den Websites und Wiederherstellen der APP mit dem Namen ContosoRestore mit der APP unserer Wahl, indem Sie Restore mit ID aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d187-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="5d187-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5d187-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="5d187-124">Wenn zwei gelöschte apps mit dem gleichen Namen (ContosoApp) vorhanden sind, erhalten Sie Details zu den Websites und zur Wiederherstellung der APP mit dem Namen ContosoRestore mit der APP unserer Wahl, indem Sie RESTORE with Inputobject (Deletedsite)-Details aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d187-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="5d187-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d187-125">PARAMETERS</span></span>

### <span data-ttu-id="5d187-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d187-126">-AsJob</span></span>
<span data-ttu-id="5d187-127">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5d187-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d187-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d187-128">-DefaultProfile</span></span>
<span data-ttu-id="5d187-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d187-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d187-130">-Gelöschte-Nr</span><span class="sxs-lookup"><span data-stu-id="5d187-130">-DeletedId</span></span>
<span data-ttu-id="5d187-131">Die ID der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-132">-Force</span><span class="sxs-lookup"><span data-stu-id="5d187-132">-Force</span></span>
<span data-ttu-id="5d187-133">Führen Sie die Wiederherstellung ohne Aufforderung zur Bestätigung durch.</span><span class="sxs-lookup"><span data-stu-id="5d187-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5d187-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d187-134">-InputObject</span></span>
<span data-ttu-id="5d187-135">Die gelöschte Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-136">-Standort</span><span class="sxs-lookup"><span data-stu-id="5d187-136">-Location</span></span>
<span data-ttu-id="5d187-137">Der Speicherort der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5d187-138">-Name</span></span>
<span data-ttu-id="5d187-139">Der Name der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d187-140">-ResourceGroupName</span></span>
<span data-ttu-id="5d187-141">Die Ressourcengruppe der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="5d187-142">-RestoreContentOnly</span></span>
<span data-ttu-id="5d187-143">Stellen Sie die Dateien der Web-App wieder her, aber die Einstellungen werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5d187-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="5d187-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="5d187-144">-Slot</span></span>
<span data-ttu-id="5d187-145">Der gelöschte Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="5d187-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="5d187-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="5d187-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="5d187-147">Der APP-Service Plan für die neue Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-148">-Zielname</span><span class="sxs-lookup"><span data-stu-id="5d187-148">-TargetName</span></span>
<span data-ttu-id="5d187-149">Der Name der neuen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d187-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="5d187-151">Die Ressourcengruppe mit der neuen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d187-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="5d187-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="5d187-152">-TargetSlot</span></span>
<span data-ttu-id="5d187-153">Der Name des neuen Azure Web App-Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="5d187-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="5d187-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="5d187-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="5d187-155">Verwenden Sie diese Option zum Wiederherstellen einer gelöschten App aus einer Offline skalierten Einheit.</span><span class="sxs-lookup"><span data-stu-id="5d187-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="5d187-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d187-156">-Confirm</span></span>
<span data-ttu-id="5d187-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d187-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d187-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d187-158">-WhatIf</span></span>
<span data-ttu-id="5d187-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d187-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d187-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d187-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d187-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d187-161">CommonParameters</span></span>
<span data-ttu-id="5d187-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d187-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d187-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d187-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d187-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d187-164">INPUTS</span></span>

### <span data-ttu-id="5d187-165">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5d187-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="5d187-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d187-166">OUTPUTS</span></span>

### <span data-ttu-id="5d187-167">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5d187-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5d187-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d187-168">NOTES</span></span>

## <span data-ttu-id="5d187-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d187-169">RELATED LINKS</span></span>

[<span data-ttu-id="5d187-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5d187-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)