---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471381"
---
# <span data-ttu-id="32eeb-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="32eeb-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="32eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="32eeb-103">Ruft eine Automatisierungsverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="32eeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32eeb-104">SYNTAX</span></span>

### <span data-ttu-id="32eeb-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="32eeb-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32eeb-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="32eeb-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32eeb-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="32eeb-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32eeb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32eeb-108">DESCRIPTION</span></span>
<span data-ttu-id="32eeb-109">Das **Cmdlet "Get-AzAutomationConnection"** ruft mindestens eine Azure-Automatisierungsverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="32eeb-110">Standardmäßig ruft dieses Cmdlet alle Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="32eeb-111">Geben Sie den Namen einer Verbindung an, um eine bestimmte Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="32eeb-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="32eeb-112">Geben Sie den Namen des Verbindungstyps an, um alle Verbindungen eines bestimmten Typs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="32eeb-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="32eeb-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32eeb-113">EXAMPLES</span></span>

### <span data-ttu-id="32eeb-114">Beispiel 1: Alle Verbindungen erhalten</span><span class="sxs-lookup"><span data-stu-id="32eeb-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="32eeb-115">Dieser Befehl ruft Metadaten für alle Verbindungen im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="32eeb-116">Beispiel 2: Alle Verbindungen eines Typs erhalten</span><span class="sxs-lookup"><span data-stu-id="32eeb-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="32eeb-117">Dieser Befehl ruft Metadaten für Verbindungen im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="32eeb-118">Dieser Befehl ruft Verbindungen vom Typ "SqlServer" ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="32eeb-119">Beispiel 3: Herstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="32eeb-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="32eeb-120">Dieser Befehl ruft Metadaten für die Verbindung namens "ContosoConnection" ab.</span><span class="sxs-lookup"><span data-stu-id="32eeb-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="32eeb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32eeb-121">PARAMETERS</span></span>

### <span data-ttu-id="32eeb-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32eeb-122">-AutomationAccountName</span></span>
<span data-ttu-id="32eeb-123">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="32eeb-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="32eeb-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="32eeb-124">-ConnectionTypeName</span></span>
<span data-ttu-id="32eeb-125">Gibt den Namen eines Verbindungstyps an, für den dieses Cmdlet Verbindungen abruft.</span><span class="sxs-lookup"><span data-stu-id="32eeb-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="32eeb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eeb-126">-DefaultProfile</span></span>
<span data-ttu-id="32eeb-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="32eeb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32eeb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="32eeb-128">-Name</span></span>
<span data-ttu-id="32eeb-129">Gibt den Namen einer Verbindung an, die von diesem Cmdlet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="32eeb-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="32eeb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32eeb-130">-ResourceGroupName</span></span>
<span data-ttu-id="32eeb-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="32eeb-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="32eeb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eeb-132">CommonParameters</span></span>
<span data-ttu-id="32eeb-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32eeb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32eeb-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32eeb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eeb-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32eeb-135">INPUTS</span></span>

### <span data-ttu-id="32eeb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="32eeb-136">System.String</span></span>

## <span data-ttu-id="32eeb-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32eeb-137">OUTPUTS</span></span>

### <span data-ttu-id="32eeb-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="32eeb-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="32eeb-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="32eeb-139">NOTES</span></span>

## <span data-ttu-id="32eeb-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="32eeb-140">RELATED LINKS</span></span>

[<span data-ttu-id="32eeb-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="32eeb-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="32eeb-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="32eeb-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


