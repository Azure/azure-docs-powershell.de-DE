---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658510"
---
# <span data-ttu-id="e80fb-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e80fb-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="e80fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e80fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e80fb-103">Stellt eine gelöschte Web-App in einer neuen oder vorhandenen Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="e80fb-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="e80fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e80fb-104">SYNTAX</span></span>

### <span data-ttu-id="e80fb-105">FromDeletedResourceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e80fb-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e80fb-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="e80fb-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e80fb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e80fb-107">DESCRIPTION</span></span>
<span data-ttu-id="e80fb-108">Das Cmdlet **Restore-AzDeletedWebApp** stellt eine gelöschte Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="e80fb-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="e80fb-109">Die von TargetResourceGroupName, TargetName und TargetSlot angegebene Web-App wird mit den Inhalten und Einstellungen der gelöschten Web-App überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e80fb-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="e80fb-110">Wenn die Zielparameter nicht angegeben werden, werden Sie automatisch mit der Ressourcengruppe, dem Namen und dem Slot der gelöschten Web App gefüllt.</span><span class="sxs-lookup"><span data-stu-id="e80fb-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="e80fb-111">Wenn die Ziel-Web-App nicht vorhanden ist, wird Sie automatisch im App-Service Plan erstellt, der von TargetAppServicePlanName angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e80fb-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="e80fb-112">Der RestoreContentOnly-Parameter kann verwendet werden, um nur die gelöschten APP-Dateien ohne die App-Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e80fb-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="e80fb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e80fb-113">EXAMPLES</span></span>

### <span data-ttu-id="e80fb-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e80fb-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="e80fb-115">Stellt eine gelöschte App mit dem Namen ContosoApp wieder her, die zur Ressourcengruppe Standard-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="e80fb-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e80fb-116">Eine neue APP mit dem gleichen Namen und der gleichen Ressourcengruppe wird im App-Service Plan mit dem Namen ContosoPlan erstellt, und die Dateien und Einstellungen der gelöschten App werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="e80fb-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="e80fb-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e80fb-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="e80fb-118">Stellt den Staging-Slot einer gelöschten App mit dem Namen ContosoApp wieder her, die zur Ressourcengruppe Standard-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="e80fb-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e80fb-119">Die Web-App mit dem Namen ContosoRestore, die zum Standard-Web-eastus der Ressourcengruppe gehört, wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e80fb-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="e80fb-120">Die Einstellungen für gelöschte Web App werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="e80fb-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="e80fb-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e80fb-121">PARAMETERS</span></span>

### <span data-ttu-id="e80fb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e80fb-122">-AsJob</span></span>
<span data-ttu-id="e80fb-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e80fb-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e80fb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80fb-124">-DefaultProfile</span></span>
<span data-ttu-id="e80fb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e80fb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e80fb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e80fb-126">-Force</span></span>
<span data-ttu-id="e80fb-127">Führen Sie die Wiederherstellung ohne Aufforderung zur Bestätigung durch.</span><span class="sxs-lookup"><span data-stu-id="e80fb-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e80fb-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e80fb-128">-InputObject</span></span>
<span data-ttu-id="e80fb-129">Die gelöschte Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e80fb-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="e80fb-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e80fb-130">-Name</span></span>
<span data-ttu-id="e80fb-131">Der Name der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e80fb-131">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="e80fb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80fb-132">-ResourceGroupName</span></span>
<span data-ttu-id="e80fb-133">Die Ressourcengruppe der gelöschten Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e80fb-133">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="e80fb-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="e80fb-134">-RestoreContentOnly</span></span>
<span data-ttu-id="e80fb-135">Stellen Sie die Dateien der Web-App wieder her, aber die Einstellungen werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="e80fb-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="e80fb-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="e80fb-136">-Slot</span></span>
<span data-ttu-id="e80fb-137">Der gelöschte Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="e80fb-137">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="e80fb-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="e80fb-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="e80fb-139">Der APP-Service Plan für die neue Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e80fb-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="e80fb-140">-Zielname</span><span class="sxs-lookup"><span data-stu-id="e80fb-140">-TargetName</span></span>
<span data-ttu-id="e80fb-141">Der Name der neuen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e80fb-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="e80fb-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80fb-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="e80fb-143">Die Ressourcengruppe mit der neuen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e80fb-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="e80fb-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="e80fb-144">-TargetSlot</span></span>
<span data-ttu-id="e80fb-145">Der Name des neuen Azure Web App-Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="e80fb-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="e80fb-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="e80fb-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="e80fb-147">Verwenden Sie diese Option zum Wiederherstellen einer gelöschten App aus einer Offline skalierten Einheit.</span><span class="sxs-lookup"><span data-stu-id="e80fb-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="e80fb-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e80fb-148">-Confirm</span></span>
<span data-ttu-id="e80fb-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e80fb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e80fb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e80fb-150">-WhatIf</span></span>
<span data-ttu-id="e80fb-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e80fb-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e80fb-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e80fb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e80fb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80fb-153">CommonParameters</span></span>
<span data-ttu-id="e80fb-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80fb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80fb-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e80fb-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80fb-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e80fb-156">INPUTS</span></span>

### <span data-ttu-id="e80fb-157">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e80fb-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="e80fb-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e80fb-158">OUTPUTS</span></span>

### <span data-ttu-id="e80fb-159">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e80fb-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e80fb-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="e80fb-160">NOTES</span></span>

## <span data-ttu-id="e80fb-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e80fb-161">RELATED LINKS</span></span>

[<span data-ttu-id="e80fb-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e80fb-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)