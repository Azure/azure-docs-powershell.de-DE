---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504597"
---
# <span data-ttu-id="e412c-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e412c-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="e412c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e412c-102">SYNOPSIS</span></span>
<span data-ttu-id="e412c-103">Entfernt eine Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e412c-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e412c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e412c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e412c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e412c-105">DESCRIPTION</span></span>
<span data-ttu-id="e412c-106">Das Cmdlet **Remove-AzureRmAutomationConnection** entfernt eine Verbindung aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="e412c-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="e412c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e412c-107">EXAMPLES</span></span>

### <span data-ttu-id="e412c-108">Beispiel 1: Entfernen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="e412c-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e412c-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen ContosoConnection im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e412c-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e412c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e412c-110">PARAMETERS</span></span>

### <span data-ttu-id="e412c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e412c-111">-AutomationAccountName</span></span>
<span data-ttu-id="e412c-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="e412c-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e412c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e412c-113">-DefaultProfile</span></span>
<span data-ttu-id="e412c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e412c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e412c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e412c-115">-Force</span></span>
<span data-ttu-id="e412c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e412c-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e412c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e412c-117">-Name</span></span>
<span data-ttu-id="e412c-118">Gibt den Namen der Verbindung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="e412c-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e412c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e412c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e412c-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="e412c-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="e412c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e412c-121">-Confirm</span></span>
<span data-ttu-id="e412c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e412c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e412c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e412c-123">-WhatIf</span></span>
<span data-ttu-id="e412c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e412c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e412c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e412c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e412c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e412c-126">CommonParameters</span></span>
<span data-ttu-id="e412c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e412c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e412c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e412c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e412c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e412c-129">INPUTS</span></span>

### <span data-ttu-id="e412c-130">Keine</span><span class="sxs-lookup"><span data-stu-id="e412c-130">None</span></span>
<span data-ttu-id="e412c-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e412c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e412c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e412c-132">OUTPUTS</span></span>

## <span data-ttu-id="e412c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e412c-133">NOTES</span></span>

## <span data-ttu-id="e412c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e412c-134">RELATED LINKS</span></span>

[<span data-ttu-id="e412c-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e412c-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="e412c-136">Neu – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e412c-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


