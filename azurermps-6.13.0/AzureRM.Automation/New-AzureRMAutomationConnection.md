---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: e86e25cb4752bf6899e1a00fcbccb596b64f8482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482578"
---
# <span data-ttu-id="065a0-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="065a0-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="065a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="065a0-102">SYNOPSIS</span></span>
<span data-ttu-id="065a0-103">Erstellt eine Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="065a0-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="065a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="065a0-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="065a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="065a0-105">DESCRIPTION</span></span>
<span data-ttu-id="065a0-106">Das Cmdlet **New-AzureRmAutomationConnection** erstellt eine Verbindung in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="065a0-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="065a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="065a0-107">EXAMPLES</span></span>

### <span data-ttu-id="065a0-108">Beispiel 1: Erstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="065a0-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="065a0-109">Der erste Befehl weist der $FieldValue Variablen eine Hashtabelle mit Feldwerten zu.</span><span class="sxs-lookup"><span data-stu-id="065a0-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="065a0-110">Der zweite Befehl erstellt eine Azure-Verbindung mit dem Namen Connection12 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="065a0-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="065a0-111">Der Befehl verwendet die Werte für das Verbindungsfeld in $fieldValues.</span><span class="sxs-lookup"><span data-stu-id="065a0-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="065a0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="065a0-112">PARAMETERS</span></span>

### <span data-ttu-id="065a0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="065a0-113">-AutomationAccountName</span></span>
<span data-ttu-id="065a0-114">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="065a0-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="065a0-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="065a0-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="065a0-116">Gibt eine Hashtabelle an, die Schlüssel-Wert-Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="065a0-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="065a0-117">Die Schlüsselstellen die Verbindungsfelder für den angegebenen Verbindungstyp dar.</span><span class="sxs-lookup"><span data-stu-id="065a0-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="065a0-118">Die Werte stellen die spezifischen Werte für jedes Verbindungsfeld für die Verbindungsinstanz dar.</span><span class="sxs-lookup"><span data-stu-id="065a0-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065a0-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="065a0-119">-ConnectionTypeName</span></span>
<span data-ttu-id="065a0-120">Gibt den Namen des Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="065a0-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065a0-121">-DefaultProfile</span></span>
<span data-ttu-id="065a0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="065a0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="065a0-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="065a0-123">-Description</span></span>
<span data-ttu-id="065a0-124">Gibt eine Beschreibung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="065a0-124">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065a0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="065a0-125">-Name</span></span>
<span data-ttu-id="065a0-126">Gibt einen Namen für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="065a0-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="065a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="065a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="065a0-128">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="065a0-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="065a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065a0-129">CommonParameters</span></span>
<span data-ttu-id="065a0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="065a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065a0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="065a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065a0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="065a0-132">INPUTS</span></span>

### <span data-ttu-id="065a0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="065a0-133">System.String</span></span>

### <span data-ttu-id="065a0-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="065a0-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="065a0-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="065a0-135">OUTPUTS</span></span>

### <span data-ttu-id="065a0-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="065a0-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="065a0-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="065a0-137">NOTES</span></span>

## <span data-ttu-id="065a0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="065a0-138">RELATED LINKS</span></span>

[<span data-ttu-id="065a0-139">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="065a0-139">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="065a0-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="065a0-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


