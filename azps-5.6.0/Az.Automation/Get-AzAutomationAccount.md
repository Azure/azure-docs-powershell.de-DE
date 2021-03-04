---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: f88ff018f38040573783aff58287b4788017566a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942016"
---
# <span data-ttu-id="ef511-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef511-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="ef511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef511-102">SYNOPSIS</span></span>
<span data-ttu-id="ef511-103">Ruft Automatisierungskonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ef511-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="ef511-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef511-104">SYNTAX</span></span>

### <span data-ttu-id="ef511-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef511-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef511-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef511-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef511-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef511-107">DESCRIPTION</span></span>
<span data-ttu-id="ef511-108">Das **Get-AzAutomationAccount-Cmdlet** ruft Azure Automation-Konten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ef511-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="ef511-109">Weitere Informationen zu Automatisierungskonten finden Sie im New-AzAutomationAccount Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef511-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ef511-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef511-110">EXAMPLES</span></span>

### <span data-ttu-id="ef511-111">Beispiel 1: Alle Konten erhalten</span><span class="sxs-lookup"><span data-stu-id="ef511-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="ef511-112">Dieser Befehl ruft alle Automatisierungskonten in der Ressourcengruppe "ResourceGroup03" ab.</span><span class="sxs-lookup"><span data-stu-id="ef511-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="ef511-113">Beispiel 2: Ein Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="ef511-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="ef511-114">Dieser Befehl ruft das Automatisierungskonto mit dem Namen ContosoAutomationAccount in der Ressourcengruppe "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="ef511-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="ef511-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ef511-115">PARAMETERS</span></span>

### <span data-ttu-id="ef511-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef511-116">-DefaultProfile</span></span>
<span data-ttu-id="ef511-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ef511-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef511-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ef511-118">-Name</span></span>
<span data-ttu-id="ef511-119">Gibt den Namen des Automatisierungskontos an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ef511-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef511-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef511-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef511-121">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Automatisierungskonten erhält.</span><span class="sxs-lookup"><span data-stu-id="ef511-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef511-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef511-122">CommonParameters</span></span>
<span data-ttu-id="ef511-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef511-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef511-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef511-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef511-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef511-125">INPUTS</span></span>

### <span data-ttu-id="ef511-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ef511-126">System.String</span></span>

## <span data-ttu-id="ef511-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef511-127">OUTPUTS</span></span>

### <span data-ttu-id="ef511-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef511-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ef511-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ef511-129">NOTES</span></span>

## <span data-ttu-id="ef511-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ef511-130">RELATED LINKS</span></span>

[<span data-ttu-id="ef511-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef511-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="ef511-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef511-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="ef511-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef511-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


