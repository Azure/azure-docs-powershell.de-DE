---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 2964102dbb3f12b797d3d551f7bd4097ca8836a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497965"
---
# <span data-ttu-id="0799e-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0799e-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="0799e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0799e-102">SYNOPSIS</span></span>
<span data-ttu-id="0799e-103">Erstellt eine Automatisierungs Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0799e-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0799e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0799e-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0799e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0799e-105">DESCRIPTION</span></span>
<span data-ttu-id="0799e-106">Das Cmdlet **New-AzureRmAutomationConnection** erstellt eine Verbindung in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="0799e-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="0799e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0799e-107">EXAMPLES</span></span>

### <span data-ttu-id="0799e-108">Beispiel 1: Erstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="0799e-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0799e-109">Der erste Befehl weist der $FieldValue Variablen eine Hashtabelle mit Feldwerten zu.</span><span class="sxs-lookup"><span data-stu-id="0799e-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="0799e-110">Der zweite Befehl erstellt eine Azure-Verbindung mit dem Namen Connection12 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="0799e-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="0799e-111">Der Befehl verwendet die Werte für das Verbindungsfeld in $fieldValues.</span><span class="sxs-lookup"><span data-stu-id="0799e-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="0799e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0799e-112">PARAMETERS</span></span>

### <span data-ttu-id="0799e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0799e-113">-AutomationAccountName</span></span>
<span data-ttu-id="0799e-114">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="0799e-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="0799e-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="0799e-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="0799e-116">Gibt eine Hashtabelle an, die Schlüssel-Wert-Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="0799e-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="0799e-117">Die Schlüsselstellen die Verbindungsfelder für den angegebenen Verbindungstyp dar.</span><span class="sxs-lookup"><span data-stu-id="0799e-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="0799e-118">Die Werte stellen die spezifischen Werte für jedes Verbindungsfeld für die Verbindungsinstanz dar.</span><span class="sxs-lookup"><span data-stu-id="0799e-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="0799e-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="0799e-119">-ConnectionTypeName</span></span>
<span data-ttu-id="0799e-120">Gibt den Namen des Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="0799e-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="0799e-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0799e-121">-Description</span></span>
<span data-ttu-id="0799e-122">Gibt eine Beschreibung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="0799e-122">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="0799e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0799e-123">-Name</span></span>
<span data-ttu-id="0799e-124">Gibt einen Namen für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="0799e-124">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="0799e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0799e-125">-ResourceGroupName</span></span>
<span data-ttu-id="0799e-126">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="0799e-126">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="0799e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0799e-127">-DefaultProfile</span></span>
<span data-ttu-id="0799e-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0799e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0799e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0799e-129">CommonParameters</span></span>
<span data-ttu-id="0799e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0799e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0799e-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0799e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0799e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0799e-132">INPUTS</span></span>

## <span data-ttu-id="0799e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0799e-133">OUTPUTS</span></span>

### <span data-ttu-id="0799e-134">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="0799e-134">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="0799e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0799e-135">NOTES</span></span>

## <span data-ttu-id="0799e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0799e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0799e-137">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0799e-137">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="0799e-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0799e-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


