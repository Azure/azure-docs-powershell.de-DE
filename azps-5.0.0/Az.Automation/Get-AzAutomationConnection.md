---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176343"
---
# <span data-ttu-id="46a78-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="46a78-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="46a78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46a78-102">SYNOPSIS</span></span>
<span data-ttu-id="46a78-103">Ruft eine Automatisierungs Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="46a78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46a78-104">SYNTAX</span></span>

### <span data-ttu-id="46a78-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="46a78-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46a78-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="46a78-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46a78-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="46a78-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46a78-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46a78-108">DESCRIPTION</span></span>
<span data-ttu-id="46a78-109">Das Cmdlet " **Get-AzAutomationConnection** " Ruft eine oder mehrere Azure-Automatisierungs Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="46a78-110">Standardmäßig ruft dieses Cmdlet alle Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="46a78-111">Geben Sie den Namen einer Verbindung an, um eine bestimmte Verbindung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46a78-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="46a78-112">Geben Sie den Namen des Verbindungstyps an, um alle Verbindungen eines bestimmten Typs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="46a78-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="46a78-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46a78-113">EXAMPLES</span></span>

### <span data-ttu-id="46a78-114">Beispiel 1: Abrufen aller Verbindungen</span><span class="sxs-lookup"><span data-stu-id="46a78-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="46a78-115">Dieser Befehl ruft Metadaten für alle Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="46a78-116">Beispiel 2: Abrufen aller Verbindungen eines Typs</span><span class="sxs-lookup"><span data-stu-id="46a78-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="46a78-117">Dieser Befehl ruft Metadaten für Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="46a78-118">Dieser Befehl ruft Verbindungen des Typs SQLServer ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="46a78-119">Beispiel 3: Abrufen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="46a78-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="46a78-120">Dieser Befehl ruft Metadaten für die Verbindung mit dem Namen ContosoConnection ab.</span><span class="sxs-lookup"><span data-stu-id="46a78-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="46a78-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="46a78-121">PARAMETERS</span></span>

### <span data-ttu-id="46a78-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="46a78-122">-AutomationAccountName</span></span>
<span data-ttu-id="46a78-123">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="46a78-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="46a78-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="46a78-124">-ConnectionTypeName</span></span>
<span data-ttu-id="46a78-125">Gibt den Namen eines Verbindungstyps an, für den dieses Cmdlet Verbindungen abruft.</span><span class="sxs-lookup"><span data-stu-id="46a78-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="46a78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a78-126">-DefaultProfile</span></span>
<span data-ttu-id="46a78-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46a78-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46a78-128">-Name</span><span class="sxs-lookup"><span data-stu-id="46a78-128">-Name</span></span>
<span data-ttu-id="46a78-129">Gibt den Namen einer Verbindung an, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="46a78-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="46a78-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a78-130">-ResourceGroupName</span></span>
<span data-ttu-id="46a78-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="46a78-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="46a78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a78-132">CommonParameters</span></span>
<span data-ttu-id="46a78-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a78-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a78-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a78-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46a78-135">INPUTS</span></span>

### <span data-ttu-id="46a78-136">System. String</span><span class="sxs-lookup"><span data-stu-id="46a78-136">System.String</span></span>

## <span data-ttu-id="46a78-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46a78-137">OUTPUTS</span></span>

### <span data-ttu-id="46a78-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="46a78-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="46a78-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="46a78-139">NOTES</span></span>

## <span data-ttu-id="46a78-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46a78-140">RELATED LINKS</span></span>

[<span data-ttu-id="46a78-141">Neu – AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="46a78-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="46a78-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="46a78-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


