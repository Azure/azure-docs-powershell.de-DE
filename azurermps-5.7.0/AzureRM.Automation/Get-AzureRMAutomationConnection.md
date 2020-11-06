---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 85d2e5d3044efe97eef2b4aa784d8767973682f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478798"
---
# <span data-ttu-id="62bdf-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="62bdf-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="62bdf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="62bdf-103">Ruft eine Automatisierungs Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62bdf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62bdf-104">SYNTAX</span></span>

### <span data-ttu-id="62bdf-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="62bdf-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62bdf-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="62bdf-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62bdf-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="62bdf-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bdf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="62bdf-109">Das Cmdlet " **Get-AzureRmAutomationConnection** " Ruft eine oder mehrere Azure-Automatisierungs Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="62bdf-110">Standardmäßig ruft dieses Cmdlet alle Verbindungen ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="62bdf-111">Geben Sie den Namen einer Verbindung an, um eine bestimmte Verbindung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="62bdf-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="62bdf-112">Geben Sie den Namen des Verbindungstyps an, um alle Verbindungen eines bestimmten Typs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="62bdf-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="62bdf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62bdf-113">EXAMPLES</span></span>

### <span data-ttu-id="62bdf-114">Beispiel 1: Abrufen aller Verbindungen</span><span class="sxs-lookup"><span data-stu-id="62bdf-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="62bdf-115">Dieser Befehl ruft Metadaten für alle Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="62bdf-116">Beispiel 2: Abrufen aller Verbindungen eines Typs</span><span class="sxs-lookup"><span data-stu-id="62bdf-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="62bdf-117">Dieser Befehl ruft Metadaten für Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="62bdf-118">Dieser Befehl ruft Verbindungen des Typs SQLServer ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="62bdf-119">Beispiel 3: Abrufen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="62bdf-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="62bdf-120">Dieser Befehl ruft Metadaten für die Verbindung mit dem Namen ContosoConnection ab.</span><span class="sxs-lookup"><span data-stu-id="62bdf-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="62bdf-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="62bdf-121">PARAMETERS</span></span>

### <span data-ttu-id="62bdf-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62bdf-122">-AutomationAccountName</span></span>
<span data-ttu-id="62bdf-123">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="62bdf-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="62bdf-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="62bdf-124">-ConnectionTypeName</span></span>
<span data-ttu-id="62bdf-125">Gibt den Namen eines Verbindungstyps an, für den dieses Cmdlet Verbindungen abruft.</span><span class="sxs-lookup"><span data-stu-id="62bdf-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62bdf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bdf-126">-DefaultProfile</span></span>
<span data-ttu-id="62bdf-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="62bdf-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62bdf-128">-Name</span><span class="sxs-lookup"><span data-stu-id="62bdf-128">-Name</span></span>
<span data-ttu-id="62bdf-129">Gibt den Namen einer Verbindung an, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="62bdf-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62bdf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bdf-130">-ResourceGroupName</span></span>
<span data-ttu-id="62bdf-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="62bdf-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="62bdf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bdf-132">CommonParameters</span></span>
<span data-ttu-id="62bdf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bdf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bdf-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bdf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bdf-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62bdf-135">INPUTS</span></span>

### <span data-ttu-id="62bdf-136">Keine</span><span class="sxs-lookup"><span data-stu-id="62bdf-136">None</span></span>
<span data-ttu-id="62bdf-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="62bdf-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62bdf-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62bdf-138">OUTPUTS</span></span>

### <span data-ttu-id="62bdf-139">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="62bdf-139">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="62bdf-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="62bdf-140">NOTES</span></span>

## <span data-ttu-id="62bdf-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62bdf-141">RELATED LINKS</span></span>

[<span data-ttu-id="62bdf-142">Neu – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="62bdf-142">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="62bdf-143">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="62bdf-143">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


