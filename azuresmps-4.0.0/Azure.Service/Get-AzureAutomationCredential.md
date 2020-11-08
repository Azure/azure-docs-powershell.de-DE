---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005865"
---
# <span data-ttu-id="34fb2-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="34fb2-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="34fb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34fb2-102">SYNOPSIS</span></span>

<span data-ttu-id="34fb2-103">Ruft eine Azure-Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="34fb2-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="34fb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34fb2-104">SYNTAX</span></span>

### <span data-ttu-id="34fb2-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="34fb2-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="34fb2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="34fb2-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="34fb2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34fb2-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="34fb2-108">Das Cmdlet " **Get-AzureAutomationCredential** " ruft mindestens eine Microsoft Azure-Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="34fb2-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="34fb2-109">Standardmäßig werden alle Anmeldeinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34fb2-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="34fb2-110">Um eine bestimmte Anmeldeinformationen abzurufen, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="34fb2-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="34fb2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34fb2-111">EXAMPLES</span></span>

### <span data-ttu-id="34fb2-112">Beispiel 1: Abrufen aller Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="34fb2-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="34fb2-113">Dieser Befehl ruft alle Anmeldeinformationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="34fb2-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="34fb2-114">Beispiel 2: Abrufen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="34fb2-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="34fb2-115">Dieser Befehl ruft die Anmeldeinformationen mit dem Namen myCredential ab.</span><span class="sxs-lookup"><span data-stu-id="34fb2-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="34fb2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="34fb2-116">PARAMETERS</span></span>

### <span data-ttu-id="34fb2-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34fb2-117">-AutomationAccountName</span></span>
<span data-ttu-id="34fb2-118">Gibt den Namen des Automatisierungs Kontos mit den Anmeldeinformationen an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34fb2-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="34fb2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="34fb2-119">-Name</span></span>
<span data-ttu-id="34fb2-120">Gibt den Namen der abzurufenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="34fb2-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34fb2-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="34fb2-121">-Profile</span></span>
<span data-ttu-id="34fb2-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="34fb2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34fb2-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="34fb2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34fb2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34fb2-124">CommonParameters</span></span>
<span data-ttu-id="34fb2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34fb2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34fb2-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34fb2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34fb2-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34fb2-127">INPUTS</span></span>

## <span data-ttu-id="34fb2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34fb2-128">OUTPUTS</span></span>

### <span data-ttu-id="34fb2-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="34fb2-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="34fb2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="34fb2-130">NOTES</span></span>

## <span data-ttu-id="34fb2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34fb2-131">RELATED LINKS</span></span>

[<span data-ttu-id="34fb2-132">Neu – AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="34fb2-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="34fb2-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="34fb2-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="34fb2-134">Satz-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="34fb2-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


