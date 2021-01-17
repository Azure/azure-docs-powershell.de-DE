---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471337"
---
# <span data-ttu-id="40408-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="40408-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="40408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40408-102">SYNOPSIS</span></span>
<span data-ttu-id="40408-103">Ruft eine Liste der Azure Automation-Quellsteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="40408-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="40408-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40408-104">SYNTAX</span></span>

### <span data-ttu-id="40408-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="40408-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40408-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40408-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40408-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40408-107">DESCRIPTION</span></span>
<span data-ttu-id="40408-108">Das Get-AzAutomationSourceControl cmdlet ruft die Automatisierungsquellensteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="40408-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="40408-109">Um ein bestimmtes Quellsteuerelement zu erhalten, geben Sie dessen Namen an.</span><span class="sxs-lookup"><span data-stu-id="40408-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="40408-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40408-110">EXAMPLES</span></span>

### <span data-ttu-id="40408-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40408-111">Example 1</span></span>
<span data-ttu-id="40408-112">Dieser Befehl ruft ein Automatisierungsquellensteuerelement namens VSTSNative im Konto mit dem Namen "devAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="40408-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="40408-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40408-113">PARAMETERS</span></span>

### <span data-ttu-id="40408-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40408-114">-AutomationAccountName</span></span>
<span data-ttu-id="40408-115">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="40408-115">The automation account name.</span></span>

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

### <span data-ttu-id="40408-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40408-116">-DefaultProfile</span></span>
<span data-ttu-id="40408-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40408-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40408-118">-Name</span><span class="sxs-lookup"><span data-stu-id="40408-118">-Name</span></span>
<span data-ttu-id="40408-119">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="40408-119">The source control name.</span></span>

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

### <span data-ttu-id="40408-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40408-120">-ResourceGroupName</span></span>
<span data-ttu-id="40408-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40408-121">The resource group name.</span></span>

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

### <span data-ttu-id="40408-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="40408-122">-SourceType</span></span>
<span data-ttu-id="40408-123">Der Typ des Quellcodeverwaltungssteuerelements.</span><span class="sxs-lookup"><span data-stu-id="40408-123">The source control type.</span></span>

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

### <span data-ttu-id="40408-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40408-124">CommonParameters</span></span>
<span data-ttu-id="40408-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40408-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40408-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40408-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40408-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40408-127">INPUTS</span></span>

### <span data-ttu-id="40408-128">System.String</span><span class="sxs-lookup"><span data-stu-id="40408-128">System.String</span></span>

## <span data-ttu-id="40408-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40408-129">OUTPUTS</span></span>

### <span data-ttu-id="40408-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="40408-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="40408-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40408-131">NOTES</span></span>

## <span data-ttu-id="40408-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40408-132">RELATED LINKS</span></span>
