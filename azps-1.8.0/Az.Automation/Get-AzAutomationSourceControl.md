---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: e960b1d68b57ef51ef51a6bd00365242e78f47a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661797"
---
# <span data-ttu-id="d224d-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="d224d-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="d224d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d224d-102">SYNOPSIS</span></span>
<span data-ttu-id="d224d-103">Ruft eine Liste der Azure Automation-Quellsteuer Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="d224d-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="d224d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d224d-104">SYNTAX</span></span>

### <span data-ttu-id="d224d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="d224d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d224d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d224d-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d224d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d224d-107">DESCRIPTION</span></span>
<span data-ttu-id="d224d-108">Das Get-AzAutomationSourceControl-Cmdlet ruft Steuerelemente für die Automatisierungs Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="d224d-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="d224d-109">Um ein bestimmtes Quellsteuerelement abzurufen, geben Sie dessen Namen an.</span><span class="sxs-lookup"><span data-stu-id="d224d-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="d224d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d224d-110">EXAMPLES</span></span>

### <span data-ttu-id="d224d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d224d-111">Example 1</span></span>
<span data-ttu-id="d224d-112">Dieser Befehl ruft ein Automatisierungs Quellen-Steuerelement mit dem Namen VSTSNative im Konto mit dem Namen devAccount.</span><span class="sxs-lookup"><span data-stu-id="d224d-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="d224d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d224d-113">PARAMETERS</span></span>

### <span data-ttu-id="d224d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d224d-114">-AutomationAccountName</span></span>
<span data-ttu-id="d224d-115">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="d224d-115">The automation account name.</span></span>

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

### <span data-ttu-id="d224d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d224d-116">-DefaultProfile</span></span>
<span data-ttu-id="d224d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d224d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d224d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d224d-118">-Name</span></span>
<span data-ttu-id="d224d-119">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="d224d-119">The source control name.</span></span>

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

### <span data-ttu-id="d224d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d224d-120">-ResourceGroupName</span></span>
<span data-ttu-id="d224d-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d224d-121">The resource group name.</span></span>

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

### <span data-ttu-id="d224d-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d224d-122">-SourceType</span></span>
<span data-ttu-id="d224d-123">Der Typ des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="d224d-123">The source control type.</span></span>

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

### <span data-ttu-id="d224d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d224d-124">CommonParameters</span></span>
<span data-ttu-id="d224d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d224d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d224d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d224d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d224d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d224d-127">INPUTS</span></span>

### <span data-ttu-id="d224d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d224d-128">System.String</span></span>

## <span data-ttu-id="d224d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d224d-129">OUTPUTS</span></span>

### <span data-ttu-id="d224d-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="d224d-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="d224d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d224d-131">NOTES</span></span>

## <span data-ttu-id="d224d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d224d-132">RELATED LINKS</span></span>
