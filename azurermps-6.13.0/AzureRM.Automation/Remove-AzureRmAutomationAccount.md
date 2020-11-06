---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: e3dd0d475a2a2c34dfa7912bf9ced4ef958295c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480622"
---
# <span data-ttu-id="5a8c8-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5a8c8-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="5a8c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8c8-103">Entfernt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a8c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a8c8-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a8c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="5a8c8-106">Das Cmdlet **Remove-AzureRmAutomationAccount** entfernt ein Azure Automation-Konto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="5a8c8-107">Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzureRmAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="5a8c8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a8c8-108">EXAMPLES</span></span>

### <span data-ttu-id="5a8c8-109">Beispiel 1: Entfernen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="5a8c8-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5a8c8-110">Mit diesem Befehl wird ein Automatisierungs Kontonamens ContosoAutomationAccount entfernt, ohne dass die Benutzerüberprüfung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="5a8c8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a8c8-111">PARAMETERS</span></span>

### <span data-ttu-id="5a8c8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8c8-112">-DefaultProfile</span></span>
<span data-ttu-id="5a8c8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5a8c8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a8c8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5a8c8-114">-Force</span></span>
<span data-ttu-id="5a8c8-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="5a8c8-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8c8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a8c8-116">-Name</span></span>
<span data-ttu-id="5a8c8-117">Gibt den Namen des Automatisierungs Kontos an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8c8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a8c8-118">-ResourceGroupName</span></span>
<span data-ttu-id="5a8c8-119">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet ein Automatisierungs Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="5a8c8-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a8c8-120">-Confirm</span></span>
<span data-ttu-id="5a8c8-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a8c8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a8c8-122">-WhatIf</span></span>
<span data-ttu-id="5a8c8-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a8c8-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a8c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8c8-125">CommonParameters</span></span>
<span data-ttu-id="5a8c8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a8c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8c8-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a8c8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8c8-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a8c8-128">INPUTS</span></span>

### <span data-ttu-id="5a8c8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5a8c8-129">System.String</span></span>

## <span data-ttu-id="5a8c8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a8c8-130">OUTPUTS</span></span>

### <span data-ttu-id="5a8c8-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5a8c8-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="5a8c8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a8c8-132">NOTES</span></span>

## <span data-ttu-id="5a8c8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a8c8-133">RELATED LINKS</span></span>

[<span data-ttu-id="5a8c8-134">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5a8c8-134">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="5a8c8-135">Neu – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5a8c8-135">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="5a8c8-136">Satz-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5a8c8-136">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


