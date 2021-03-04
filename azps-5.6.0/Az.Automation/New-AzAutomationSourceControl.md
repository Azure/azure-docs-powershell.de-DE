---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: d9fbbed1beb67ce1bc8732cb5641c78705fd6a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920864"
---
# <span data-ttu-id="830f5-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="830f5-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="830f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="830f5-102">SYNOPSIS</span></span>
<span data-ttu-id="830f5-103">Erstellt ein A Automation-Quellsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="830f5-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="830f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="830f5-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830f5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="830f5-105">DESCRIPTION</span></span>
<span data-ttu-id="830f5-106">Das New-AzAutomationSourceControl-Cmdlet erstellt eine Konfiguration, um mein Azure Automation-Konto mit meinem VSTS TFVC, VSTS Git oder GitHub zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="830f5-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="830f5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="830f5-107">EXAMPLES</span></span>

### <span data-ttu-id="830f5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="830f5-108">Example 1</span></span>
<span data-ttu-id="830f5-109">Erstellen Sie eine Quellsteuerelementkonfiguration, um mein Azure Automation-Konto mit meinem VSTS TFVC-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="830f5-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="830f5-110">TFVC-Projekte haben keine Verzweigungen, daher wird der Parameter "Verzweigung" nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="830f5-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="830f5-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="830f5-111">Example 2</span></span>
<span data-ttu-id="830f5-112">Erstellen Sie eine Quellsteuerelementkonfiguration, um mein Azure Automation-Konto mit meinem VSTS-Git-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="830f5-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="830f5-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="830f5-113">Example 3</span></span>
<span data-ttu-id="830f5-114">Erstellen Sie eine Quellsteuerelementkonfiguration, um mein Azure Automation-Konto mit meinem GitHub-Projekt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="830f5-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="830f5-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="830f5-115">PARAMETERS</span></span>

### <span data-ttu-id="830f5-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="830f5-116">-AccessToken</span></span>
<span data-ttu-id="830f5-117">Das Zugriffstoken für das Quellsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="830f5-117">The source control access token.</span></span>

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

### <span data-ttu-id="830f5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="830f5-118">-AutomationAccountName</span></span>
<span data-ttu-id="830f5-119">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="830f5-119">The automation account name.</span></span>

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

### <span data-ttu-id="830f5-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="830f5-120">-Branch</span></span>
<span data-ttu-id="830f5-121">Der Quellcodeverwaltungszweig.</span><span class="sxs-lookup"><span data-stu-id="830f5-121">The source control branch.</span></span>

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

### <span data-ttu-id="830f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830f5-122">-DefaultProfile</span></span>
<span data-ttu-id="830f5-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="830f5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830f5-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="830f5-124">-Description</span></span>
<span data-ttu-id="830f5-125">Die Beschreibung des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="830f5-125">The source control description.</span></span>

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

### <span data-ttu-id="830f5-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="830f5-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="830f5-127">Die publishRunbook-Eigenschaft des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="830f5-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="830f5-128">Wenn DoNotPublishRunbook festgelegt ist, bedeutet dies, dass Benutzer-Runbooks als "Entwurf" importiert werden.</span><span class="sxs-lookup"><span data-stu-id="830f5-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="830f5-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="830f5-129">-EnableAutoSync</span></span>
<span data-ttu-id="830f5-130">Die autoSync-Eigenschaft für das Quellsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="830f5-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="830f5-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="830f5-131">-FolderPath</span></span>
<span data-ttu-id="830f5-132">Der Ordnerpfad des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="830f5-132">The source control folder path.</span></span>

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

### <span data-ttu-id="830f5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="830f5-133">-Name</span></span>
<span data-ttu-id="830f5-134">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="830f5-134">The source control name.</span></span>

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

### <span data-ttu-id="830f5-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="830f5-135">-RepoUrl</span></span>
<span data-ttu-id="830f5-136">Die Quellsteuerelement-Repository-URL.</span><span class="sxs-lookup"><span data-stu-id="830f5-136">The source control repo url.</span></span>

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

### <span data-ttu-id="830f5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="830f5-137">-ResourceGroupName</span></span>
<span data-ttu-id="830f5-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="830f5-138">The resource group name.</span></span>

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

### <span data-ttu-id="830f5-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="830f5-139">-SourceType</span></span>
<span data-ttu-id="830f5-140">Der Typ des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="830f5-140">The source control type.</span></span>

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

### <span data-ttu-id="830f5-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="830f5-141">-Confirm</span></span>
<span data-ttu-id="830f5-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="830f5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="830f5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830f5-143">-WhatIf</span></span>
<span data-ttu-id="830f5-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="830f5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="830f5-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="830f5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830f5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830f5-146">CommonParameters</span></span>
<span data-ttu-id="830f5-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830f5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830f5-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830f5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830f5-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="830f5-149">INPUTS</span></span>

### <span data-ttu-id="830f5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="830f5-150">System.String</span></span>

## <span data-ttu-id="830f5-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="830f5-151">OUTPUTS</span></span>

### <span data-ttu-id="830f5-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="830f5-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="830f5-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="830f5-153">NOTES</span></span>

## <span data-ttu-id="830f5-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="830f5-154">RELATED LINKS</span></span>
