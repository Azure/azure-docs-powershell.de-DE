---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006430"
---
# <span data-ttu-id="2655f-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2655f-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="2655f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2655f-102">SYNOPSIS</span></span>

<span data-ttu-id="2655f-103">Erstellt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="2655f-103">Creates an Automation account.</span></span>

## <span data-ttu-id="2655f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2655f-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2655f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2655f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2655f-106">Das Cmdlet **New-AzureAutomationAccount** erstellt ein neues Konto in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2655f-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="2655f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2655f-107">EXAMPLES</span></span>

### <span data-ttu-id="2655f-108">Beispiel 1: Erstellen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="2655f-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="2655f-109">Dieser Befehl erstellt ein Automatisierungs Konto mit dem Namen MyAutomationAccount in der Region Ost-USA.</span><span class="sxs-lookup"><span data-stu-id="2655f-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="2655f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2655f-110">PARAMETERS</span></span>

### <span data-ttu-id="2655f-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="2655f-111">-Location</span></span>
<span data-ttu-id="2655f-112">Gibt den Standort des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2655f-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="2655f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2655f-113">-Name</span></span>
<span data-ttu-id="2655f-114">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2655f-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2655f-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="2655f-115">-Profile</span></span>
<span data-ttu-id="2655f-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2655f-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2655f-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2655f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2655f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2655f-118">CommonParameters</span></span>
<span data-ttu-id="2655f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2655f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2655f-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2655f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2655f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2655f-121">INPUTS</span></span>

## <span data-ttu-id="2655f-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2655f-122">OUTPUTS</span></span>

### <span data-ttu-id="2655f-123">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2655f-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="2655f-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="2655f-124">NOTES</span></span>

## <span data-ttu-id="2655f-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2655f-125">RELATED LINKS</span></span>

[<span data-ttu-id="2655f-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2655f-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="2655f-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2655f-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


