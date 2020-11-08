---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997420"
---
# <span data-ttu-id="f066c-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f066c-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="f066c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f066c-102">SYNOPSIS</span></span>
<span data-ttu-id="f066c-103">Ruft Automatisierungs Konten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f066c-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="f066c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f066c-104">SYNTAX</span></span>

### <span data-ttu-id="f066c-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="f066c-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f066c-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f066c-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f066c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f066c-107">DESCRIPTION</span></span>
<span data-ttu-id="f066c-108">Das Cmdlet " **Get-AzAutomationAccount** " ruft Azure Automation-Konten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f066c-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="f066c-109">Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f066c-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="f066c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f066c-110">EXAMPLES</span></span>

### <span data-ttu-id="f066c-111">Beispiel 1: Abrufen aller Konten</span><span class="sxs-lookup"><span data-stu-id="f066c-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="f066c-112">Dieser Befehl ruft alle Automatisierungs Konten in der Ressourcengruppe mit dem Namen ResourceGroup03 ab.</span><span class="sxs-lookup"><span data-stu-id="f066c-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="f066c-113">Beispiel 2: Abrufen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="f066c-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="f066c-114">Dieser Befehl ruft das Automatisierungs Konto mit dem Namen ContosoAutomationAccount in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="f066c-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="f066c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f066c-115">PARAMETERS</span></span>

### <span data-ttu-id="f066c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f066c-116">-DefaultProfile</span></span>
<span data-ttu-id="f066c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f066c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f066c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f066c-118">-Name</span></span>
<span data-ttu-id="f066c-119">Gibt den Namen des Automatisierungs Kontos an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f066c-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f066c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f066c-120">-ResourceGroupName</span></span>
<span data-ttu-id="f066c-121">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Automatisierungs Konten erhält.</span><span class="sxs-lookup"><span data-stu-id="f066c-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="f066c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f066c-122">CommonParameters</span></span>
<span data-ttu-id="f066c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f066c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f066c-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f066c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f066c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f066c-125">INPUTS</span></span>

### <span data-ttu-id="f066c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f066c-126">System.String</span></span>

## <span data-ttu-id="f066c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f066c-127">OUTPUTS</span></span>

### <span data-ttu-id="f066c-128">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f066c-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="f066c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f066c-129">NOTES</span></span>

## <span data-ttu-id="f066c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f066c-130">RELATED LINKS</span></span>

[<span data-ttu-id="f066c-131">Neu – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f066c-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="f066c-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f066c-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="f066c-133">Satz-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f066c-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


