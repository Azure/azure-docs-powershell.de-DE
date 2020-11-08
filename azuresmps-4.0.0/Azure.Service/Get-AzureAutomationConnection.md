---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006576"
---
# <span data-ttu-id="e9731-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e9731-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="e9731-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9731-102">SYNOPSIS</span></span>

<span data-ttu-id="e9731-103">Ruft eine Azure-Automatisierungs Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="e9731-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="e9731-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9731-104">SYNTAX</span></span>

### <span data-ttu-id="e9731-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9731-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9731-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="e9731-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9731-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="e9731-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9731-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9731-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e9731-109">Das Cmdlet " **Get-AzureAutomationConnection** " ruft mindestens eine Microsoft Azure-Automatisierungs Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="e9731-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="e9731-110">Standardmäßig werden alle Verbindungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9731-110">By default, all connections are returned.</span></span>
<span data-ttu-id="e9731-111">Um eine bestimmte Verbindung zu erhalten, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="e9731-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="e9731-112">Um alle Verbindungen eines bestimmten Typs abzurufen, geben Sie den Namen des Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="e9731-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="e9731-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9731-113">EXAMPLES</span></span>

### <span data-ttu-id="e9731-114">Beispiel 1: Abrufen aller Verbindungen</span><span class="sxs-lookup"><span data-stu-id="e9731-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e9731-115">Dieser Befehl ruft alle Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="e9731-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e9731-116">Beispiel 2: Abrufen aller Verbindungen eines Typs</span><span class="sxs-lookup"><span data-stu-id="e9731-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="e9731-117">Dieser Befehl ruft alle Azure-Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="e9731-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e9731-118">Beispiel 3: Abrufen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="e9731-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="e9731-119">Dieser Befehl ruft die Verbindung mit dem Namen myConnection ab.</span><span class="sxs-lookup"><span data-stu-id="e9731-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="e9731-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9731-120">PARAMETERS</span></span>

### <span data-ttu-id="e9731-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9731-121">-AutomationAccountName</span></span>
<span data-ttu-id="e9731-122">Gibt den Namen des Automatisierungs Kontos an, mit dem die Verbindung abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9731-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9731-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="e9731-123">-ConnectionTypeName</span></span>
<span data-ttu-id="e9731-124">Gibt den Namen eines Verbindungstyps für die Verbindungen an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e9731-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9731-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9731-125">-Name</span></span>
<span data-ttu-id="e9731-126">Gibt den Namen einer Verbindung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9731-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9731-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="e9731-127">-Profile</span></span>
<span data-ttu-id="e9731-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e9731-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9731-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e9731-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9731-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9731-130">CommonParameters</span></span>
<span data-ttu-id="e9731-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9731-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9731-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9731-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9731-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9731-133">INPUTS</span></span>

## <span data-ttu-id="e9731-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9731-134">OUTPUTS</span></span>

### <span data-ttu-id="e9731-135">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="e9731-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="e9731-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9731-136">NOTES</span></span>

## <span data-ttu-id="e9731-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9731-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9731-138">Neu – AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e9731-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="e9731-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e9731-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="e9731-140">Satz-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="e9731-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


