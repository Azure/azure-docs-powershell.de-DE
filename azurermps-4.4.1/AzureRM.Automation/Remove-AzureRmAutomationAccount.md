---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 1b8e480a266459b21e6c357da156b4d4bc5165e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497949"
---
# <span data-ttu-id="90756-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90756-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="90756-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90756-102">SYNOPSIS</span></span>
<span data-ttu-id="90756-103">Entfernt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="90756-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90756-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90756-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90756-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90756-105">DESCRIPTION</span></span>
<span data-ttu-id="90756-106">Das Cmdlet **Remove-AzureRmAutomationAccount** entfernt ein Azure Automation-Konto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90756-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="90756-107">Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzureRmAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90756-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="90756-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90756-108">EXAMPLES</span></span>

### <span data-ttu-id="90756-109">Beispiel 1: Entfernen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="90756-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="90756-110">Mit diesem Befehl wird ein Automatisierungs Kontonamens ContosoAutomationAccount entfernt, ohne dass die Benutzerüberprüfung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="90756-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="90756-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="90756-111">PARAMETERS</span></span>

### <span data-ttu-id="90756-112">-Force</span><span class="sxs-lookup"><span data-stu-id="90756-112">-Force</span></span>
<span data-ttu-id="90756-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="90756-113">ps_force</span></span>

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

### <span data-ttu-id="90756-114">-Name</span><span class="sxs-lookup"><span data-stu-id="90756-114">-Name</span></span>
<span data-ttu-id="90756-115">Gibt den Namen des Automatisierungs Kontos an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="90756-115">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="90756-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90756-116">-ResourceGroupName</span></span>
<span data-ttu-id="90756-117">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet ein Automatisierungs Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="90756-117">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="90756-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90756-118">-Confirm</span></span>
<span data-ttu-id="90756-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90756-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90756-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90756-120">-WhatIf</span></span>
<span data-ttu-id="90756-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90756-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90756-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90756-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90756-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90756-123">-DefaultProfile</span></span>
<span data-ttu-id="90756-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90756-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90756-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90756-125">CommonParameters</span></span>
<span data-ttu-id="90756-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90756-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90756-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90756-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90756-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90756-128">INPUTS</span></span>

## <span data-ttu-id="90756-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90756-129">OUTPUTS</span></span>

### <span data-ttu-id="90756-130">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90756-130">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="90756-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="90756-131">NOTES</span></span>

## <span data-ttu-id="90756-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90756-132">RELATED LINKS</span></span>

[<span data-ttu-id="90756-133">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90756-133">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="90756-134">Neu – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90756-134">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="90756-135">Satz-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="90756-135">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


