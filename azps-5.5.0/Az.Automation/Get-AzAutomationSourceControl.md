---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168388"
---
# <span data-ttu-id="801f3-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="801f3-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="801f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="801f3-102">SYNOPSIS</span></span>
<span data-ttu-id="801f3-103">Ruft eine Liste der Azure Automation-Quellsteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="801f3-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="801f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="801f3-104">SYNTAX</span></span>

### <span data-ttu-id="801f3-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="801f3-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="801f3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="801f3-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="801f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="801f3-107">DESCRIPTION</span></span>
<span data-ttu-id="801f3-108">Das Get-AzAutomationSourceControl-Cmdlet ruft Automatisierungsquellensteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="801f3-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="801f3-109">Um ein bestimmtes Quellsteuerelement zu erhalten, geben Sie dessen Namen an.</span><span class="sxs-lookup"><span data-stu-id="801f3-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="801f3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="801f3-110">EXAMPLES</span></span>

### <span data-ttu-id="801f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="801f3-111">Example 1</span></span>
<span data-ttu-id="801f3-112">Dieser Befehl ruft ein Automatisierungsquellensteuerelement namens VSTSNative im Konto mit dem Namen "devAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="801f3-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="801f3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="801f3-113">PARAMETERS</span></span>

### <span data-ttu-id="801f3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="801f3-114">-AutomationAccountName</span></span>
<span data-ttu-id="801f3-115">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="801f3-115">The automation account name.</span></span>

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

### <span data-ttu-id="801f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801f3-116">-DefaultProfile</span></span>
<span data-ttu-id="801f3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="801f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="801f3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="801f3-118">-Name</span></span>
<span data-ttu-id="801f3-119">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="801f3-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="801f3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="801f3-120">-ResourceGroupName</span></span>
<span data-ttu-id="801f3-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="801f3-121">The resource group name.</span></span>

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

### <span data-ttu-id="801f3-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="801f3-122">-SourceType</span></span>
<span data-ttu-id="801f3-123">Der Typ des Quellcodeverwaltungssteuerelements.</span><span class="sxs-lookup"><span data-stu-id="801f3-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801f3-124">CommonParameters</span></span>
<span data-ttu-id="801f3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801f3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="801f3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801f3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="801f3-127">INPUTS</span></span>

### <span data-ttu-id="801f3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="801f3-128">System.String</span></span>

## <span data-ttu-id="801f3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="801f3-129">OUTPUTS</span></span>

### <span data-ttu-id="801f3-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="801f3-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="801f3-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="801f3-131">NOTES</span></span>

## <span data-ttu-id="801f3-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="801f3-132">RELATED LINKS</span></span>
