---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665328"
---
# <span data-ttu-id="fd29d-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fd29d-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="fd29d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd29d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd29d-103">Ruft Automatisierungs Konten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="fd29d-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd29d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd29d-104">SYNTAX</span></span>

### <span data-ttu-id="fd29d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd29d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd29d-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd29d-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd29d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd29d-107">DESCRIPTION</span></span>
<span data-ttu-id="fd29d-108">Das Cmdlet " **Get-AzureRmAutomationAccount** " ruft Azure Automation-Konten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="fd29d-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="fd29d-109">Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzureRmAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd29d-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="fd29d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd29d-110">EXAMPLES</span></span>

### <span data-ttu-id="fd29d-111">Beispiel 1: Abrufen aller Konten</span><span class="sxs-lookup"><span data-stu-id="fd29d-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="fd29d-112">Dieser Befehl ruft alle Automatisierungs Konten in der Ressourcengruppe mit dem Namen ResourceGroup03 ab.</span><span class="sxs-lookup"><span data-stu-id="fd29d-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="fd29d-113">Beispiel 2: Abrufen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="fd29d-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="fd29d-114">Dieser Befehl ruft das Automatisierungs Konto mit dem Namen ContosoAutomationAccount in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="fd29d-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="fd29d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd29d-115">PARAMETERS</span></span>

### <span data-ttu-id="fd29d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd29d-116">-DefaultProfile</span></span>
<span data-ttu-id="fd29d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fd29d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd29d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fd29d-118">-Name</span></span>
<span data-ttu-id="fd29d-119">Gibt den Namen des Automatisierungs Kontos an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="fd29d-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd29d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd29d-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd29d-121">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Automatisierungs Konten erhält.</span><span class="sxs-lookup"><span data-stu-id="fd29d-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd29d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd29d-122">CommonParameters</span></span>
<span data-ttu-id="fd29d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd29d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd29d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd29d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd29d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd29d-125">INPUTS</span></span>

### <span data-ttu-id="fd29d-126">Keine</span><span class="sxs-lookup"><span data-stu-id="fd29d-126">None</span></span>
<span data-ttu-id="fd29d-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fd29d-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd29d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd29d-128">OUTPUTS</span></span>

### <span data-ttu-id="fd29d-129">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fd29d-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="fd29d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd29d-130">NOTES</span></span>

## <span data-ttu-id="fd29d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd29d-131">RELATED LINKS</span></span>

[<span data-ttu-id="fd29d-132">Neu – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fd29d-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="fd29d-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fd29d-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="fd29d-134">Satz-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fd29d-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


