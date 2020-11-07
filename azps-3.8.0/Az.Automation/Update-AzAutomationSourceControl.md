---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: ee3b7b7cdbe098c6892782ca4084bd2fb7e6a615
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846312"
---
# <span data-ttu-id="22c3a-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="22c3a-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="22c3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="22c3a-103">Aktualisiert ein Azure Automation-Quellcodeverwaltungs-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="22c3a-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="22c3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22c3a-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="22c3a-106">Das Update-AzAutomationSourceControl-Cmdlet ändert den Wert eines Felds in einer Quellcodeverwaltung in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="22c3a-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="22c3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="22c3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22c3a-108">Example 1</span></span>
<span data-ttu-id="22c3a-109">Mit diesen Befehlen wird das PublishRunbook-Feld für das Azure Automation-Quellsteuerelement namens VSTSNative im Konto mit dem Namen "devAccount" auf "false" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22c3a-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="22c3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c3a-110">PARAMETERS</span></span>

### <span data-ttu-id="22c3a-111">-Access Token</span><span class="sxs-lookup"><span data-stu-id="22c3a-111">-AccessToken</span></span>
<span data-ttu-id="22c3a-112">Das Zugriffstoken für die Quellcodeverwaltung</span><span class="sxs-lookup"><span data-stu-id="22c3a-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22c3a-113">-AutomationAccountName</span></span>
<span data-ttu-id="22c3a-114">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="22c3a-114">The automation account name.</span></span>

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

### <span data-ttu-id="22c3a-115">– AutoSync</span><span class="sxs-lookup"><span data-stu-id="22c3a-115">-AutoSync</span></span>
<span data-ttu-id="22c3a-116">Die AutoSync-Eigenschaft für das Quellcodeverwaltungs-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="22c3a-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3a-117">-Branch</span><span class="sxs-lookup"><span data-stu-id="22c3a-117">-Branch</span></span>
<span data-ttu-id="22c3a-118">Die Quellcodeverwaltungsverzweigung.</span><span class="sxs-lookup"><span data-stu-id="22c3a-118">The source control branch.</span></span>

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

### <span data-ttu-id="22c3a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c3a-119">-DefaultProfile</span></span>
<span data-ttu-id="22c3a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22c3a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c3a-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22c3a-121">-Description</span></span>
<span data-ttu-id="22c3a-122">Beschreibung der Quellcodeverwaltung</span><span class="sxs-lookup"><span data-stu-id="22c3a-122">The source control description.</span></span>

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

### <span data-ttu-id="22c3a-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="22c3a-123">-FolderPath</span></span>
<span data-ttu-id="22c3a-124">Der Pfad des Quellcodeverwaltungsordners.</span><span class="sxs-lookup"><span data-stu-id="22c3a-124">The source control folder path.</span></span>

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

### <span data-ttu-id="22c3a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="22c3a-125">-Name</span></span>
<span data-ttu-id="22c3a-126">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="22c3a-126">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c3a-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="22c3a-127">-PublishRunbook</span></span>
<span data-ttu-id="22c3a-128">Die publishRunbook-Eigenschaft des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="22c3a-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c3a-129">-ResourceGroupName</span></span>
<span data-ttu-id="22c3a-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="22c3a-130">The resource group name.</span></span>

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

### <span data-ttu-id="22c3a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22c3a-131">-Confirm</span></span>
<span data-ttu-id="22c3a-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22c3a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c3a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c3a-133">-WhatIf</span></span>
<span data-ttu-id="22c3a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22c3a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22c3a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22c3a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c3a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c3a-136">CommonParameters</span></span>
<span data-ttu-id="22c3a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c3a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c3a-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c3a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c3a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22c3a-139">INPUTS</span></span>

### <span data-ttu-id="22c3a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="22c3a-140">System.String</span></span>

## <span data-ttu-id="22c3a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22c3a-141">OUTPUTS</span></span>

### <span data-ttu-id="22c3a-142">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="22c3a-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="22c3a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="22c3a-143">NOTES</span></span>

## <span data-ttu-id="22c3a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22c3a-144">RELATED LINKS</span></span>
