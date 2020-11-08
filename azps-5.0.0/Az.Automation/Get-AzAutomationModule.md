---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178345"
---
# <span data-ttu-id="8f481-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f481-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="8f481-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f481-102">SYNOPSIS</span></span>
<span data-ttu-id="8f481-103">Ruft Metadaten für Module aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="8f481-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="8f481-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f481-104">SYNTAX</span></span>

### <span data-ttu-id="8f481-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f481-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f481-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8f481-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f481-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f481-107">DESCRIPTION</span></span>
<span data-ttu-id="8f481-108">Das Cmdlet " **Get-AzAutomationModule** " ruft Metadaten für Module aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="8f481-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="8f481-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f481-109">EXAMPLES</span></span>

### <span data-ttu-id="8f481-110">Beispiel 1: Abrufen aller Module</span><span class="sxs-lookup"><span data-stu-id="8f481-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f481-111">Dieser Befehl ruft alle Module im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8f481-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8f481-112">Beispiel 2: Abrufen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="8f481-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f481-113">Dieser Befehl ruft ein Modul mit dem Namen ContosoModule im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8f481-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8f481-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f481-114">PARAMETERS</span></span>

### <span data-ttu-id="8f481-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f481-115">-AutomationAccountName</span></span>
<span data-ttu-id="8f481-116">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Modul Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8f481-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="8f481-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f481-117">-DefaultProfile</span></span>
<span data-ttu-id="8f481-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f481-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f481-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8f481-119">-Name</span></span>
<span data-ttu-id="8f481-120">Gibt den Namen des Moduls an, für das dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8f481-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f481-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f481-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f481-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Modul Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8f481-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="8f481-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f481-123">CommonParameters</span></span>
<span data-ttu-id="8f481-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f481-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f481-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f481-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f481-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f481-126">INPUTS</span></span>

### <span data-ttu-id="8f481-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8f481-127">System.String</span></span>

## <span data-ttu-id="8f481-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f481-128">OUTPUTS</span></span>

### <span data-ttu-id="8f481-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="8f481-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="8f481-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f481-130">NOTES</span></span>

## <span data-ttu-id="8f481-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f481-131">RELATED LINKS</span></span>

[<span data-ttu-id="8f481-132">Neu – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f481-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="8f481-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f481-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="8f481-134">Satz-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f481-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


