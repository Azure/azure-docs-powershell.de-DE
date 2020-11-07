---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661779"
---
# <span data-ttu-id="dd346-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dd346-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="dd346-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd346-102">SYNOPSIS</span></span>
<span data-ttu-id="dd346-103">Erstellt eine Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="dd346-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="dd346-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd346-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd346-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd346-105">DESCRIPTION</span></span>
<span data-ttu-id="dd346-106">Das Cmdlet **New-AzAutomationConnection** erstellt eine Verbindung in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="dd346-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="dd346-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd346-107">EXAMPLES</span></span>

### <span data-ttu-id="dd346-108">Beispiel 1: Erstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="dd346-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="dd346-109">Der erste Befehl weist der $FieldValue Variablen eine Hashtabelle mit Feldwerten zu.</span><span class="sxs-lookup"><span data-stu-id="dd346-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="dd346-110">Der zweite Befehl erstellt eine Azure-Verbindung mit dem Namen Connection12 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="dd346-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="dd346-111">Der Befehl verwendet die Werte für das Verbindungsfeld in $fieldValues.</span><span class="sxs-lookup"><span data-stu-id="dd346-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="dd346-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd346-112">PARAMETERS</span></span>

### <span data-ttu-id="dd346-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd346-113">-AutomationAccountName</span></span>
<span data-ttu-id="dd346-114">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="dd346-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="dd346-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="dd346-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="dd346-116">Gibt eine Hashtabelle an, die Schlüssel-Wert-Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="dd346-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="dd346-117">Die Schlüsselstellen die Verbindungsfelder für den angegebenen Verbindungstyp dar.</span><span class="sxs-lookup"><span data-stu-id="dd346-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="dd346-118">Die Werte stellen die spezifischen Werte für jedes Verbindungsfeld für die Verbindungsinstanz dar.</span><span class="sxs-lookup"><span data-stu-id="dd346-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="dd346-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="dd346-119">-ConnectionTypeName</span></span>
<span data-ttu-id="dd346-120">Gibt den Namen des Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="dd346-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="dd346-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd346-121">-DefaultProfile</span></span>
<span data-ttu-id="dd346-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dd346-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd346-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd346-123">-Description</span></span>
<span data-ttu-id="dd346-124">Gibt eine Beschreibung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="dd346-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="dd346-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dd346-125">-Name</span></span>
<span data-ttu-id="dd346-126">Gibt einen Namen für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="dd346-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="dd346-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd346-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd346-128">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="dd346-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="dd346-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd346-129">CommonParameters</span></span>
<span data-ttu-id="dd346-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd346-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd346-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd346-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd346-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd346-132">INPUTS</span></span>

### <span data-ttu-id="dd346-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd346-133">System.String</span></span>

### <span data-ttu-id="dd346-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="dd346-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="dd346-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd346-135">OUTPUTS</span></span>

### <span data-ttu-id="dd346-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="dd346-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="dd346-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd346-137">NOTES</span></span>

## <span data-ttu-id="dd346-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd346-138">RELATED LINKS</span></span>

[<span data-ttu-id="dd346-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dd346-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="dd346-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dd346-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


