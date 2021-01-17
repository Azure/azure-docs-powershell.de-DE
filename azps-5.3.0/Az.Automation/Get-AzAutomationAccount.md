---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471391"
---
# <span data-ttu-id="e26b6-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e26b6-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="e26b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e26b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e26b6-103">Ruft Automatisierungskonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e26b6-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="e26b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e26b6-104">SYNTAX</span></span>

### <span data-ttu-id="e26b6-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="e26b6-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e26b6-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e26b6-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26b6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e26b6-107">DESCRIPTION</span></span>
<span data-ttu-id="e26b6-108">Das **Get-AzAutomationAccount-Cmdlet** ruft Azure-Automatisierungskonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e26b6-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="e26b6-109">Weitere Informationen zu Automatisierungskonten finden Sie im New-AzAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e26b6-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e26b6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e26b6-110">EXAMPLES</span></span>

### <span data-ttu-id="e26b6-111">Beispiel 1: Alle Konten erhalten</span><span class="sxs-lookup"><span data-stu-id="e26b6-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="e26b6-112">Dieser Befehl ruft alle Automatisierungskonten in der Ressourcengruppe mit dem Namen "ResourceGroup03" ab.</span><span class="sxs-lookup"><span data-stu-id="e26b6-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="e26b6-113">Beispiel 2: Erhalten eines Kontos</span><span class="sxs-lookup"><span data-stu-id="e26b6-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="e26b6-114">Dieser Befehl ruft das Automatisierungskonto namens "ContosoAutomationAccount" in der Ressourcengruppe mit dem Namen "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="e26b6-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="e26b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e26b6-115">PARAMETERS</span></span>

### <span data-ttu-id="e26b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26b6-116">-DefaultProfile</span></span>
<span data-ttu-id="e26b6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e26b6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e26b6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e26b6-118">-Name</span></span>
<span data-ttu-id="e26b6-119">Gibt den Namen des Automatisierungskontos an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e26b6-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e26b6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e26b6-120">-ResourceGroupName</span></span>
<span data-ttu-id="e26b6-121">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Automatisierungskonten erhält.</span><span class="sxs-lookup"><span data-stu-id="e26b6-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="e26b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26b6-122">CommonParameters</span></span>
<span data-ttu-id="e26b6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26b6-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26b6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26b6-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e26b6-125">INPUTS</span></span>

### <span data-ttu-id="e26b6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e26b6-126">System.String</span></span>

## <span data-ttu-id="e26b6-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e26b6-127">OUTPUTS</span></span>

### <span data-ttu-id="e26b6-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e26b6-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e26b6-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e26b6-129">NOTES</span></span>

## <span data-ttu-id="e26b6-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e26b6-130">RELATED LINKS</span></span>

[<span data-ttu-id="e26b6-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e26b6-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="e26b6-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e26b6-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="e26b6-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e26b6-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


