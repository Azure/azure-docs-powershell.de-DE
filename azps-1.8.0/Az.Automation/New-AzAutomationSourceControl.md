---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 86a3df5cca859befbe1eabb65424269d11edf8e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661763"
---
# <span data-ttu-id="d7b36-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="d7b36-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="d7b36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7b36-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b36-103">Erstellt ein Automatisierungs Quellen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d7b36-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="d7b36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b36-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b36-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b36-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b36-106">Das New-AzAutomationSourceControl-Cmdlet erstellt eine Konfiguration zum Verknüpfen meines Azure-Automatisierungs Kontos mit meinem VSTS-TFVC, VSTS git oder GitHub.</span><span class="sxs-lookup"><span data-stu-id="d7b36-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="d7b36-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7b36-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b36-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7b36-108">Example 1</span></span>
<span data-ttu-id="d7b36-109">Erstellen Sie eine Quellcodeverwaltungs-Konfiguration, um mein Azure Automation-Konto mit meinem VSTS-TFVC-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d7b36-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="d7b36-110">TFVC-Projekte verfügen nicht über Verzweigungen, und daher wird der Branch-Parameter nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d7b36-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

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

### <span data-ttu-id="d7b36-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d7b36-111">Example 2</span></span>
<span data-ttu-id="d7b36-112">Erstellen Sie eine Quellcodeverwaltungs-Konfiguration, um mein Azure-Automatisierungs Konto mit meinem VSTS git-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d7b36-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


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

### <span data-ttu-id="d7b36-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d7b36-113">Example 3</span></span>
<span data-ttu-id="d7b36-114">Erstellen Sie eine Quellcodeverwaltungs-Konfiguration, um mein Azure Automation-Konto mit meinem github-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d7b36-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="d7b36-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7b36-115">PARAMETERS</span></span>

### <span data-ttu-id="d7b36-116">-Access Token</span><span class="sxs-lookup"><span data-stu-id="d7b36-116">-AccessToken</span></span>
<span data-ttu-id="d7b36-117">Das Zugriffstoken für die Quellcodeverwaltung</span><span class="sxs-lookup"><span data-stu-id="d7b36-117">The source control access token.</span></span>

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

### <span data-ttu-id="d7b36-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d7b36-118">-AutomationAccountName</span></span>
<span data-ttu-id="d7b36-119">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="d7b36-119">The automation account name.</span></span>

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

### <span data-ttu-id="d7b36-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="d7b36-120">-Branch</span></span>
<span data-ttu-id="d7b36-121">Die Quellcodeverwaltungsverzweigung.</span><span class="sxs-lookup"><span data-stu-id="d7b36-121">The source control branch.</span></span>

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

### <span data-ttu-id="d7b36-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b36-122">-DefaultProfile</span></span>
<span data-ttu-id="d7b36-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7b36-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b36-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b36-124">-Description</span></span>
<span data-ttu-id="d7b36-125">Beschreibung der Quellcodeverwaltung</span><span class="sxs-lookup"><span data-stu-id="d7b36-125">The source control description.</span></span>

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

### <span data-ttu-id="d7b36-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="d7b36-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="d7b36-127">Die publishRunbook-Eigenschaft des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="d7b36-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="d7b36-128">Wenn DoNotPublishRunbook festgelegt ist, bedeutet dies, dass Benutzer runbooks als "Entwurf" importiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7b36-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="d7b36-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="d7b36-129">-EnableAutoSync</span></span>
<span data-ttu-id="d7b36-130">Die AutoSync-Eigenschaft für das Quellcodeverwaltungs-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d7b36-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="d7b36-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="d7b36-131">-FolderPath</span></span>
<span data-ttu-id="d7b36-132">Der Pfad des Quellcodeverwaltungsordners.</span><span class="sxs-lookup"><span data-stu-id="d7b36-132">The source control folder path.</span></span>

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

### <span data-ttu-id="d7b36-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b36-133">-Name</span></span>
<span data-ttu-id="d7b36-134">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="d7b36-134">The source control name.</span></span>

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

### <span data-ttu-id="d7b36-135">-Repourl</span><span class="sxs-lookup"><span data-stu-id="d7b36-135">-RepoUrl</span></span>
<span data-ttu-id="d7b36-136">Die Repository-URL für die Quellcodeverwaltung</span><span class="sxs-lookup"><span data-stu-id="d7b36-136">The source control repo url.</span></span>

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

### <span data-ttu-id="d7b36-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b36-137">-ResourceGroupName</span></span>
<span data-ttu-id="d7b36-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7b36-138">The resource group name.</span></span>

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

### <span data-ttu-id="d7b36-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d7b36-139">-SourceType</span></span>
<span data-ttu-id="d7b36-140">Der Typ des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="d7b36-140">The source control type.</span></span>

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

### <span data-ttu-id="d7b36-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7b36-141">-Confirm</span></span>
<span data-ttu-id="d7b36-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7b36-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b36-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b36-143">-WhatIf</span></span>
<span data-ttu-id="d7b36-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b36-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b36-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7b36-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b36-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b36-146">CommonParameters</span></span>
<span data-ttu-id="d7b36-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b36-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b36-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b36-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b36-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7b36-149">INPUTS</span></span>

### <span data-ttu-id="d7b36-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b36-150">System.String</span></span>

## <span data-ttu-id="d7b36-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7b36-151">OUTPUTS</span></span>

### <span data-ttu-id="d7b36-152">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="d7b36-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="d7b36-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7b36-153">NOTES</span></span>

## <span data-ttu-id="d7b36-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7b36-154">RELATED LINKS</span></span>
