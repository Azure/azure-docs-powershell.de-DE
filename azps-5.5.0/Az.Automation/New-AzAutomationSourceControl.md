---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168241"
---
# <span data-ttu-id="5587d-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="5587d-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="5587d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5587d-102">SYNOPSIS</span></span>
<span data-ttu-id="5587d-103">Erstellt ein Automatisierungsquellensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="5587d-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="5587d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5587d-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5587d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5587d-105">DESCRIPTION</span></span>
<span data-ttu-id="5587d-106">Das New-AzAutomationSourceControl erstellt eine Konfiguration, um mein Azure-Automatisierungskonto mit VSTS TFVC, VSTS Git oder GitHub zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5587d-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="5587d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5587d-107">EXAMPLES</span></span>

### <span data-ttu-id="5587d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5587d-108">Example 1</span></span>
<span data-ttu-id="5587d-109">Erstellen Sie eine Quellcodeverwaltungskonfiguration, um mein Azure-Automatisierungskonto mit meinem VSTS -TFVC-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5587d-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="5587d-110">Bei EINEM TFVC-Projekt gibt es keine Verzweigungen, daher wird der Parameter "Branch" nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="5587d-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="5587d-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5587d-111">Example 2</span></span>
<span data-ttu-id="5587d-112">Erstellen Sie eine Quellcodeverwaltungskonfiguration, um mein Azure-Automatisierungskonto mit meinem VSTS-Git-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5587d-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="5587d-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5587d-113">Example 3</span></span>
<span data-ttu-id="5587d-114">Erstellen Sie eine Quellcodeverwaltungskonfiguration, um mein Azure-Automatisierungskonto mit meinem GitHub-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5587d-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="5587d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5587d-115">PARAMETERS</span></span>

### <span data-ttu-id="5587d-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="5587d-116">-AccessToken</span></span>
<span data-ttu-id="5587d-117">Das Zugriffstoken für die Quellcodeverwaltung.</span><span class="sxs-lookup"><span data-stu-id="5587d-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5587d-118">-AutomationAccountName</span></span>
<span data-ttu-id="5587d-119">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="5587d-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="5587d-120">-Branch</span></span>
<span data-ttu-id="5587d-121">Die Verzweigung des Quellcodeverwaltungssteuerelements.</span><span class="sxs-lookup"><span data-stu-id="5587d-121">The source control branch.</span></span>

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

### <span data-ttu-id="5587d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5587d-122">-DefaultProfile</span></span>
<span data-ttu-id="5587d-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5587d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5587d-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5587d-124">-Description</span></span>
<span data-ttu-id="5587d-125">Beschreibung des Quellcodeverwaltungssteuerelements</span><span class="sxs-lookup"><span data-stu-id="5587d-125">The source control description.</span></span>

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

### <span data-ttu-id="5587d-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="5587d-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="5587d-127">Die "publishRunbook"-Eigenschaft des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="5587d-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="5587d-128">Wenn "DoNotPublishRunbook" festgelegt ist, bedeutet dies, dass Benutzerlaufbücher als "Entwurf" importiert werden.</span><span class="sxs-lookup"><span data-stu-id="5587d-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="5587d-129">-EnableAutoSync</span></span>
<span data-ttu-id="5587d-130">Die "autoSync"-Eigenschaft für das Quellsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="5587d-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="5587d-131">-FolderPath</span></span>
<span data-ttu-id="5587d-132">Der Pfad des Quellcodeverwaltungsordners.</span><span class="sxs-lookup"><span data-stu-id="5587d-132">The source control folder path.</span></span>

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

### <span data-ttu-id="5587d-133">-Name</span><span class="sxs-lookup"><span data-stu-id="5587d-133">-Name</span></span>
<span data-ttu-id="5587d-134">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="5587d-134">The source control name.</span></span>

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

### <span data-ttu-id="5587d-135">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="5587d-135">-RepoUrl</span></span>
<span data-ttu-id="5587d-136">Die Repository-URL des Quellcodeverwaltungssteuerelements.</span><span class="sxs-lookup"><span data-stu-id="5587d-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5587d-137">-ResourceGroupName</span></span>
<span data-ttu-id="5587d-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5587d-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="5587d-139">-SourceType</span></span>
<span data-ttu-id="5587d-140">Der Typ des Quellcodeverwaltungssteuerelements.</span><span class="sxs-lookup"><span data-stu-id="5587d-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5587d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5587d-141">-Confirm</span></span>
<span data-ttu-id="5587d-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5587d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5587d-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5587d-143">-WhatIf</span></span>
<span data-ttu-id="5587d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5587d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5587d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5587d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5587d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5587d-146">CommonParameters</span></span>
<span data-ttu-id="5587d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5587d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5587d-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5587d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5587d-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5587d-149">INPUTS</span></span>

### <span data-ttu-id="5587d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5587d-150">System.String</span></span>

## <span data-ttu-id="5587d-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5587d-151">OUTPUTS</span></span>

### <span data-ttu-id="5587d-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="5587d-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="5587d-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5587d-153">NOTES</span></span>

## <span data-ttu-id="5587d-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5587d-154">RELATED LINKS</span></span>
