---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006698"
---
# <span data-ttu-id="40e2b-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="40e2b-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="40e2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40e2b-102">SYNOPSIS</span></span>

<span data-ttu-id="40e2b-103">Entfernt eine Verbindung aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="40e2b-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="40e2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40e2b-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40e2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40e2b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="40e2b-106">Das Cmdlet **Remove-AzureAutomationConnection** entfernt eine Verbindung aus der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="40e2b-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="40e2b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40e2b-107">EXAMPLES</span></span>

### <span data-ttu-id="40e2b-108">Beispiel 1: Entfernen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="40e2b-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="40e2b-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen myConnection im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="40e2b-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="40e2b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="40e2b-110">PARAMETERS</span></span>

### <span data-ttu-id="40e2b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40e2b-111">-AutomationAccountName</span></span>
<span data-ttu-id="40e2b-112">Gibt den Namen des Automatisierungs Kontos mit den Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="40e2b-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="40e2b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40e2b-113">-Force</span></span>
<span data-ttu-id="40e2b-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="40e2b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e2b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="40e2b-115">-Name</span></span>
<span data-ttu-id="40e2b-116">Gibt den Namen der Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="40e2b-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="40e2b-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="40e2b-117">-Profile</span></span>
<span data-ttu-id="40e2b-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="40e2b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40e2b-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="40e2b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40e2b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e2b-120">CommonParameters</span></span>
<span data-ttu-id="40e2b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e2b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e2b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e2b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e2b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40e2b-123">INPUTS</span></span>

## <span data-ttu-id="40e2b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40e2b-124">OUTPUTS</span></span>

## <span data-ttu-id="40e2b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="40e2b-125">NOTES</span></span>

## <span data-ttu-id="40e2b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40e2b-126">RELATED LINKS</span></span>

[<span data-ttu-id="40e2b-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="40e2b-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="40e2b-128">Neu – AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="40e2b-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="40e2b-129">Satz-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="40e2b-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


