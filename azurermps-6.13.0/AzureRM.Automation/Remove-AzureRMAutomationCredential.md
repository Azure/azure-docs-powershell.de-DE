---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 6c0fe1185bfa8d5233371788da87e7a13fe32c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477986"
---
# <span data-ttu-id="84cca-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84cca-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="84cca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84cca-102">SYNOPSIS</span></span>
<span data-ttu-id="84cca-103">Entfernt eine Automatisierungs Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="84cca-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84cca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84cca-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84cca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84cca-105">DESCRIPTION</span></span>
<span data-ttu-id="84cca-106">Mit dem Cmdlet **Remove-AzureRmAutomationCredential** werden Anmeldeinformationen aus Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="84cca-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="84cca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84cca-107">EXAMPLES</span></span>

### <span data-ttu-id="84cca-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="84cca-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="84cca-109">Dieser Befehl entfernt die Anmeldeinformationen mit dem Namen ContosoCredential im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="84cca-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="84cca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="84cca-110">PARAMETERS</span></span>

### <span data-ttu-id="84cca-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="84cca-111">-AutomationAccountName</span></span>
<span data-ttu-id="84cca-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet eine Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="84cca-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="84cca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cca-113">-DefaultProfile</span></span>
<span data-ttu-id="84cca-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="84cca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="84cca-115">-Name</span></span>
<span data-ttu-id="84cca-116">Gibt den Namen der Anmeldeinformationen an, die vom Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="84cca-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84cca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84cca-117">-ResourceGroupName</span></span>
<span data-ttu-id="84cca-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="84cca-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="84cca-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84cca-119">-Confirm</span></span>
<span data-ttu-id="84cca-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84cca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84cca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84cca-121">-WhatIf</span></span>
<span data-ttu-id="84cca-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84cca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84cca-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84cca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84cca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cca-124">CommonParameters</span></span>
<span data-ttu-id="84cca-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84cca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cca-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84cca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cca-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84cca-127">INPUTS</span></span>

### <span data-ttu-id="84cca-128">System. String</span><span class="sxs-lookup"><span data-stu-id="84cca-128">System.String</span></span>

## <span data-ttu-id="84cca-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84cca-129">OUTPUTS</span></span>

### <span data-ttu-id="84cca-130">System. void</span><span class="sxs-lookup"><span data-stu-id="84cca-130">System.Void</span></span>

## <span data-ttu-id="84cca-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="84cca-131">NOTES</span></span>

## <span data-ttu-id="84cca-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84cca-132">RELATED LINKS</span></span>

[<span data-ttu-id="84cca-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84cca-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="84cca-134">Neu – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84cca-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="84cca-135">Satz-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84cca-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


