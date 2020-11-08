---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005142"
---
# <span data-ttu-id="191d8-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="191d8-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="191d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="191d8-102">SYNOPSIS</span></span>
<span data-ttu-id="191d8-103">Entfernt eine Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="191d8-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="191d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="191d8-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="191d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="191d8-105">DESCRIPTION</span></span>
<span data-ttu-id="191d8-106">Das Cmdlet **Remove-AzAutomationConnection** entfernt eine Verbindung aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="191d8-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="191d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="191d8-107">EXAMPLES</span></span>

### <span data-ttu-id="191d8-108">Beispiel 1: Entfernen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="191d8-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="191d8-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen ContosoConnection im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="191d8-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="191d8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="191d8-110">PARAMETERS</span></span>

### <span data-ttu-id="191d8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="191d8-111">-AutomationAccountName</span></span>
<span data-ttu-id="191d8-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="191d8-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="191d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191d8-113">-DefaultProfile</span></span>
<span data-ttu-id="191d8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="191d8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="191d8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="191d8-115">-Force</span></span>
<span data-ttu-id="191d8-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="191d8-116">ps_force</span></span>

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

### <span data-ttu-id="191d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="191d8-117">-Name</span></span>
<span data-ttu-id="191d8-118">Gibt den Namen der Verbindung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="191d8-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="191d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="191d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="191d8-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="191d8-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="191d8-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="191d8-121">-Confirm</span></span>
<span data-ttu-id="191d8-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="191d8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="191d8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191d8-123">-WhatIf</span></span>
<span data-ttu-id="191d8-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="191d8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="191d8-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="191d8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="191d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191d8-126">CommonParameters</span></span>
<span data-ttu-id="191d8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191d8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191d8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191d8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="191d8-129">INPUTS</span></span>

### <span data-ttu-id="191d8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="191d8-130">System.String</span></span>

## <span data-ttu-id="191d8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="191d8-131">OUTPUTS</span></span>

### <span data-ttu-id="191d8-132">System. void</span><span class="sxs-lookup"><span data-stu-id="191d8-132">System.Void</span></span>

## <span data-ttu-id="191d8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="191d8-133">NOTES</span></span>

## <span data-ttu-id="191d8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="191d8-134">RELATED LINKS</span></span>

[<span data-ttu-id="191d8-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="191d8-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="191d8-136">Neu – AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="191d8-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


