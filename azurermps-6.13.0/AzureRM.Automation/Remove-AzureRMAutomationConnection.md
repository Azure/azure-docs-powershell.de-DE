---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 570ab5c1c53f302f829a6abd57964fdffea1147d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663688"
---
# <span data-ttu-id="3e262-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3e262-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="3e262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e262-102">SYNOPSIS</span></span>
<span data-ttu-id="3e262-103">Entfernt eine Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3e262-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e262-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e262-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e262-105">DESCRIPTION</span></span>
<span data-ttu-id="3e262-106">Das Cmdlet **Remove-AzureRmAutomationConnection** entfernt eine Verbindung aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="3e262-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="3e262-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e262-107">EXAMPLES</span></span>

### <span data-ttu-id="3e262-108">Beispiel 1: Entfernen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="3e262-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3e262-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen ContosoConnection im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3e262-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3e262-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e262-110">PARAMETERS</span></span>

### <span data-ttu-id="3e262-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e262-111">-AutomationAccountName</span></span>
<span data-ttu-id="3e262-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="3e262-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="3e262-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e262-113">-DefaultProfile</span></span>
<span data-ttu-id="3e262-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3e262-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e262-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3e262-115">-Force</span></span>
<span data-ttu-id="3e262-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3e262-116">ps_force</span></span>

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

### <span data-ttu-id="3e262-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3e262-117">-Name</span></span>
<span data-ttu-id="3e262-118">Gibt den Namen der Verbindung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="3e262-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3e262-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e262-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e262-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="3e262-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="3e262-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e262-121">-Confirm</span></span>
<span data-ttu-id="3e262-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e262-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e262-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e262-123">-WhatIf</span></span>
<span data-ttu-id="3e262-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e262-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e262-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e262-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e262-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e262-126">CommonParameters</span></span>
<span data-ttu-id="3e262-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e262-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e262-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e262-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e262-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e262-129">INPUTS</span></span>

### <span data-ttu-id="3e262-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e262-130">System.String</span></span>

## <span data-ttu-id="3e262-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e262-131">OUTPUTS</span></span>

### <span data-ttu-id="3e262-132">System. void</span><span class="sxs-lookup"><span data-stu-id="3e262-132">System.Void</span></span>

## <span data-ttu-id="3e262-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e262-133">NOTES</span></span>

## <span data-ttu-id="3e262-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e262-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e262-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3e262-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="3e262-136">Neu – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3e262-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


