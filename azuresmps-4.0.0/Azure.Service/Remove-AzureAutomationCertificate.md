---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006699"
---
# <span data-ttu-id="ffef5-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffef5-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="ffef5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffef5-102">SYNOPSIS</span></span>

<span data-ttu-id="ffef5-103">Entfernt ein Automatisierungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="ffef5-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="ffef5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffef5-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ffef5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffef5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ffef5-106">Das Cmdlet **Remove-AzureAutomationAccount** entfernt ein Zertifikat aus der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ffef5-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="ffef5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffef5-107">EXAMPLES</span></span>

### <span data-ttu-id="ffef5-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="ffef5-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="ffef5-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen Cert01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ffef5-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ffef5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffef5-110">PARAMETERS</span></span>

### <span data-ttu-id="ffef5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ffef5-111">-AutomationAccountName</span></span>
<span data-ttu-id="ffef5-112">Gibt den Namen des Automatisierungs Kontos mit dem Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="ffef5-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="ffef5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ffef5-113">-Force</span></span>
<span data-ttu-id="ffef5-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ffef5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ffef5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ffef5-115">-Name</span></span>
<span data-ttu-id="ffef5-116">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="ffef5-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="ffef5-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ffef5-117">-Profile</span></span>
<span data-ttu-id="ffef5-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ffef5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ffef5-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ffef5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffef5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffef5-120">CommonParameters</span></span>
<span data-ttu-id="ffef5-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffef5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffef5-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffef5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffef5-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffef5-123">INPUTS</span></span>

## <span data-ttu-id="ffef5-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffef5-124">OUTPUTS</span></span>

## <span data-ttu-id="ffef5-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffef5-125">NOTES</span></span>

## <span data-ttu-id="ffef5-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffef5-126">RELATED LINKS</span></span>

[<span data-ttu-id="ffef5-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffef5-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="ffef5-128">Neu – AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffef5-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="ffef5-129">Satz-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffef5-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


