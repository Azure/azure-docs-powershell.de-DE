---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: bbb90e728c9c43c011c4610ee47273af1fdae668
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499078"
---
# <span data-ttu-id="0021e-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0021e-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="0021e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0021e-102">SYNOPSIS</span></span>
<span data-ttu-id="0021e-103">Ändert ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="0021e-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0021e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0021e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0021e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0021e-105">DESCRIPTION</span></span>
<span data-ttu-id="0021e-106">Das Cmdlet " **Satz-AzureRmAutomationAccount** " ändert ein Azure-Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="0021e-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="0021e-107">Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzureRmAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0021e-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="0021e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0021e-108">EXAMPLES</span></span>

### <span data-ttu-id="0021e-109">Beispiel 1: Einrichten der Tags für ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="0021e-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="0021e-110">Der erste Befehl weist der $Tags-Variablen zwei Schlüssel-Wert-Paare zu.</span><span class="sxs-lookup"><span data-stu-id="0021e-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="0021e-111">Der zweite Befehl legt Tags in $Tags für das Automatisierungs Konto mit dem Namen "AutomationAccount01" fest.</span><span class="sxs-lookup"><span data-stu-id="0021e-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="0021e-112">Beispiel 2: Ändern des Plans für ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="0021e-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="0021e-113">Dieser Befehl ändert den Plan in Basic für das Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="0021e-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="0021e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0021e-114">PARAMETERS</span></span>

### <span data-ttu-id="0021e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0021e-115">-DefaultProfile</span></span>
<span data-ttu-id="0021e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0021e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0021e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0021e-117">-Name</span></span>
<span data-ttu-id="0021e-118">Gibt den Namen des Automatisierungs Kontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0021e-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0021e-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="0021e-119">-Plan</span></span>
<span data-ttu-id="0021e-120">Gibt den Plan für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="0021e-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="0021e-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0021e-121">Valid values are:</span></span>

- <span data-ttu-id="0021e-122">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="0021e-122">Basic</span></span>
- <span data-ttu-id="0021e-123">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="0021e-123">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0021e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0021e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0021e-125">Gibt den Namen einer Ressourcengruppe an, die das Automatisierungs Konto enthält, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0021e-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0021e-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="0021e-126">-Tags</span></span>
<span data-ttu-id="0021e-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0021e-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0021e-128">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0021e-128">For example:</span></span>

<span data-ttu-id="0021e-129">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0021e-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0021e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0021e-130">CommonParameters</span></span>
<span data-ttu-id="0021e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0021e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0021e-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0021e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0021e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0021e-133">INPUTS</span></span>

### <span data-ttu-id="0021e-134">Keine</span><span class="sxs-lookup"><span data-stu-id="0021e-134">None</span></span>
<span data-ttu-id="0021e-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0021e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0021e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0021e-136">OUTPUTS</span></span>

### <span data-ttu-id="0021e-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0021e-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="0021e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0021e-138">NOTES</span></span>

## <span data-ttu-id="0021e-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0021e-139">RELATED LINKS</span></span>

[<span data-ttu-id="0021e-140">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0021e-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="0021e-141">Neu – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0021e-141">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="0021e-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0021e-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
