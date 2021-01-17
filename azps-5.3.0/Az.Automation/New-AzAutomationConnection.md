---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471317"
---
# <span data-ttu-id="89333-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="89333-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="89333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89333-102">SYNOPSIS</span></span>
<span data-ttu-id="89333-103">Erstellt eine Automatisierungsverbindung.</span><span class="sxs-lookup"><span data-stu-id="89333-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="89333-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89333-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89333-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89333-105">DESCRIPTION</span></span>
<span data-ttu-id="89333-106">Das **Cmdlet "New-AzAutomationConnection"** erstellt eine Verbindung in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="89333-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="89333-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89333-107">EXAMPLES</span></span>

### <span data-ttu-id="89333-108">Beispiel 1: Erstellen einer Verbindung für ConnectionTypeName=Azure</span><span class="sxs-lookup"><span data-stu-id="89333-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="89333-109">Der erste Befehl weist der Variablen eine Hashtabelle mit Feldwerten $FieldValue zu.</span><span class="sxs-lookup"><span data-stu-id="89333-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="89333-110">Der zweite Befehl erstellt eine Azure-Verbindung namens "Connection12" im Automatisierungskonto namens "AutomationAccount01".</span><span class="sxs-lookup"><span data-stu-id="89333-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="89333-111">Der Befehl verwendet die Verbindungsfeldwerte in $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="89333-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="89333-112">Beispiel 2: Erstellen einer Verbindung für ConnectionTypeName=AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="89333-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="89333-113">Der Befehl erstellt mithilfe von $RunAsAccountConnectionFieldValues und ConnectionTypeName=AzureServicePrincipal eine Azure-Verbindung namens "Connection13" im Automatisierungskonto namens "AutomationAccount01".</span><span class="sxs-lookup"><span data-stu-id="89333-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="89333-114">Dieser ConnectionTypeName=AzureServicePrincipal wird hauptsächlich für Azure Run As Account verwendet.</span><span class="sxs-lookup"><span data-stu-id="89333-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="89333-115">Beispiel 3: Erstellen einer Verbindung für ConnectionTypeName=AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="89333-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="89333-116">Der Befehl erstellt mithilfe von $ClassicRunAsAccountConnectionFieldValues und ConnectionTypeName=AzureClassicCertificate eine Azure-Verbindung namens "Connection14" im Automatisierungskonto namens "AutomationAccount01".</span><span class="sxs-lookup"><span data-stu-id="89333-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="89333-117">Dieser ConnectionTypeName=AzureClassicCertificate wird hauptsächlich für das klassische Azure-Konto "Ausführen als Konto" verwendet.</span><span class="sxs-lookup"><span data-stu-id="89333-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="89333-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89333-118">PARAMETERS</span></span>

### <span data-ttu-id="89333-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="89333-119">-AutomationAccountName</span></span>
<span data-ttu-id="89333-120">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet eine Verbindung erstellt.</span><span class="sxs-lookup"><span data-stu-id="89333-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="89333-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="89333-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="89333-122">Gibt eine Hashtabelle an, die Schlüssel-Wert-Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="89333-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="89333-123">Die Schlüssel stellen die Verbindungsfelder für den angegebenen Verbindungstyp dar.</span><span class="sxs-lookup"><span data-stu-id="89333-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="89333-124">Die Werte stellen die spezifischen Werte der einzelnen Verbindungsfelds für die Verbindungsinstanz dar.</span><span class="sxs-lookup"><span data-stu-id="89333-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="89333-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="89333-125">-ConnectionTypeName</span></span>
<span data-ttu-id="89333-126">Gibt den Namen des Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="89333-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="89333-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89333-127">-DefaultProfile</span></span>
<span data-ttu-id="89333-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89333-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89333-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89333-129">-Description</span></span>
<span data-ttu-id="89333-130">Gibt eine Beschreibung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="89333-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="89333-131">-Name</span><span class="sxs-lookup"><span data-stu-id="89333-131">-Name</span></span>
<span data-ttu-id="89333-132">Gibt einen Namen für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="89333-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="89333-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89333-133">-ResourceGroupName</span></span>
<span data-ttu-id="89333-134">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung erstellt.</span><span class="sxs-lookup"><span data-stu-id="89333-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="89333-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89333-135">CommonParameters</span></span>
<span data-ttu-id="89333-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89333-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89333-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89333-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89333-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89333-138">INPUTS</span></span>

### <span data-ttu-id="89333-139">System.String</span><span class="sxs-lookup"><span data-stu-id="89333-139">System.String</span></span>

### <span data-ttu-id="89333-140">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="89333-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="89333-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89333-141">OUTPUTS</span></span>

### <span data-ttu-id="89333-142">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="89333-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="89333-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89333-143">NOTES</span></span>

## <span data-ttu-id="89333-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89333-144">RELATED LINKS</span></span>

[<span data-ttu-id="89333-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="89333-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="89333-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="89333-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


