---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497933"
---
# <span data-ttu-id="56f5b-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="56f5b-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="56f5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="56f5b-103">Entfernt ein Modul aus Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="56f5b-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56f5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56f5b-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56f5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="56f5b-106">Das Cmdlet **Remove-AzureRmAutomationModule** entfernt ein Modul aus einem Automatisierungs Konto in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="56f5b-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="56f5b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="56f5b-108">Beispiel 1: Entfernen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="56f5b-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="56f5b-109">Dieser Befehl entfernt ein Modul mit dem Namen ContosoModule aus dem Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="56f5b-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="56f5b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56f5b-110">PARAMETERS</span></span>

### <span data-ttu-id="56f5b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56f5b-111">-AutomationAccountName</span></span>
<span data-ttu-id="56f5b-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="56f5b-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="56f5b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="56f5b-113">-Force</span></span>
<span data-ttu-id="56f5b-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="56f5b-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f5b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="56f5b-115">-Name</span></span>
<span data-ttu-id="56f5b-116">Gibt den Namen des Moduls an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="56f5b-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56f5b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f5b-117">-ResourceGroupName</span></span>
<span data-ttu-id="56f5b-118">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="56f5b-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="56f5b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56f5b-119">-Confirm</span></span>
<span data-ttu-id="56f5b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56f5b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56f5b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56f5b-121">-WhatIf</span></span>
<span data-ttu-id="56f5b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56f5b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56f5b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56f5b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56f5b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f5b-124">-DefaultProfile</span></span>
<span data-ttu-id="56f5b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56f5b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f5b-126">CommonParameters</span></span>
<span data-ttu-id="56f5b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f5b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f5b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f5b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56f5b-129">INPUTS</span></span>

## <span data-ttu-id="56f5b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56f5b-130">OUTPUTS</span></span>

## <span data-ttu-id="56f5b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="56f5b-131">NOTES</span></span>

## <span data-ttu-id="56f5b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56f5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="56f5b-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="56f5b-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="56f5b-134">Neu – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="56f5b-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="56f5b-135">Satz-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="56f5b-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


