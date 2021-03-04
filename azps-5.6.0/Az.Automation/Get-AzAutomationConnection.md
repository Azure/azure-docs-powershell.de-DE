---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 5332cb1ca52a8ee3e7685ecf2fd36fd2333fd453
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942011"
---
# <span data-ttu-id="5f063-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5f063-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="5f063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f063-102">SYNOPSIS</span></span>
<span data-ttu-id="5f063-103">Ruft eine Automatisierungsverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="5f063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f063-104">SYNTAX</span></span>

### <span data-ttu-id="5f063-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f063-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f063-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="5f063-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f063-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="5f063-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f063-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f063-108">DESCRIPTION</span></span>
<span data-ttu-id="5f063-109">Das **Get-AzAutomationConnection-Cmdlet** ruft mindestens eine Azure Automation-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="5f063-110">Standardmäßig ruft dieses Cmdlet alle Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="5f063-111">Geben Sie den Namen einer Verbindung an, um eine bestimmte Verbindung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f063-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="5f063-112">Geben Sie den Namen des Verbindungstyps an, um alle Verbindungen eines bestimmten Typs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f063-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="5f063-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f063-113">EXAMPLES</span></span>

### <span data-ttu-id="5f063-114">Beispiel 1: Alle Verbindungen erhalten</span><span class="sxs-lookup"><span data-stu-id="5f063-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5f063-115">Dieser Befehl ruft Metadaten für alle Verbindungen im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5f063-116">Beispiel 2: Alle Verbindungen eines Typs</span><span class="sxs-lookup"><span data-stu-id="5f063-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="5f063-117">Dieser Befehl ruft Metadaten für Verbindungen im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="5f063-118">Dieser Befehl ruft Verbindungen vom Typ SqlServer ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="5f063-119">Beispiel 3: Herstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="5f063-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="5f063-120">Dieser Befehl ruft Metadaten für die Verbindung namens ContosoConnection ab.</span><span class="sxs-lookup"><span data-stu-id="5f063-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="5f063-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f063-121">PARAMETERS</span></span>

### <span data-ttu-id="5f063-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f063-122">-AutomationAccountName</span></span>
<span data-ttu-id="5f063-123">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="5f063-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="5f063-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="5f063-124">-ConnectionTypeName</span></span>
<span data-ttu-id="5f063-125">Gibt den Namen eines Verbindungstyps an, für den dieses Cmdlet Verbindungen abruft.</span><span class="sxs-lookup"><span data-stu-id="5f063-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f063-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f063-126">-DefaultProfile</span></span>
<span data-ttu-id="5f063-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5f063-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f063-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5f063-128">-Name</span></span>
<span data-ttu-id="5f063-129">Gibt den Namen einer Verbindung an, die von diesem Cmdlet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5f063-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f063-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f063-130">-ResourceGroupName</span></span>
<span data-ttu-id="5f063-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="5f063-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="5f063-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f063-132">CommonParameters</span></span>
<span data-ttu-id="5f063-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f063-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f063-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f063-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f063-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f063-135">INPUTS</span></span>

### <span data-ttu-id="5f063-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5f063-136">System.String</span></span>

## <span data-ttu-id="5f063-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f063-137">OUTPUTS</span></span>

### <span data-ttu-id="5f063-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="5f063-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="5f063-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5f063-139">NOTES</span></span>

## <span data-ttu-id="5f063-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5f063-140">RELATED LINKS</span></span>

[<span data-ttu-id="5f063-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5f063-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="5f063-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5f063-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


