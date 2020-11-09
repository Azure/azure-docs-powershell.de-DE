---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301606"
---
# <span data-ttu-id="bd902-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bd902-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="bd902-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd902-102">SYNOPSIS</span></span>
<span data-ttu-id="bd902-103">Ändert ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="bd902-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="bd902-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd902-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd902-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd902-105">DESCRIPTION</span></span>
<span data-ttu-id="bd902-106">Das Cmdlet " **Satz-AzAutomationAccount** " ändert ein Azure-Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="bd902-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="bd902-107">Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd902-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="bd902-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd902-108">EXAMPLES</span></span>

### <span data-ttu-id="bd902-109">Beispiel 1: Einrichten der Tags für ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="bd902-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="bd902-110">Der erste Befehl weist der $Tags-Variablen zwei Schlüssel-Wert-Paare zu.</span><span class="sxs-lookup"><span data-stu-id="bd902-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="bd902-111">Der zweite Befehl legt Tags in $Tags für das Automatisierungs Konto mit dem Namen "AutomationAccount01" fest.</span><span class="sxs-lookup"><span data-stu-id="bd902-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="bd902-112">Beispiel 2: Ändern des Plans für ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="bd902-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="bd902-113">Dieser Befehl ändert den Plan in Basic für das Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="bd902-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="bd902-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd902-114">PARAMETERS</span></span>

### <span data-ttu-id="bd902-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd902-115">-DefaultProfile</span></span>
<span data-ttu-id="bd902-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bd902-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd902-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bd902-117">-Name</span></span>
<span data-ttu-id="bd902-118">Gibt den Namen des Automatisierungs Kontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bd902-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bd902-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="bd902-119">-Plan</span></span>
<span data-ttu-id="bd902-120">Gibt den Plan für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="bd902-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="bd902-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bd902-121">Valid values are:</span></span>
- <span data-ttu-id="bd902-122">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="bd902-122">Basic</span></span>
- <span data-ttu-id="bd902-123">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="bd902-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd902-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd902-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd902-125">Gibt den Namen einer Ressourcengruppe an, die das Automatisierungs Konto enthält, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bd902-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bd902-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="bd902-126">-Tags</span></span>
<span data-ttu-id="bd902-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="bd902-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bd902-128">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="bd902-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd902-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd902-129">CommonParameters</span></span>
<span data-ttu-id="bd902-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd902-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd902-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd902-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd902-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd902-132">INPUTS</span></span>

### <span data-ttu-id="bd902-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bd902-133">System.String</span></span>

### <span data-ttu-id="bd902-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bd902-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="bd902-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd902-135">OUTPUTS</span></span>

### <span data-ttu-id="bd902-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bd902-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="bd902-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd902-137">NOTES</span></span>

## <span data-ttu-id="bd902-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd902-138">RELATED LINKS</span></span>

[<span data-ttu-id="bd902-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bd902-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="bd902-140">Neu – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bd902-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="bd902-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bd902-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
