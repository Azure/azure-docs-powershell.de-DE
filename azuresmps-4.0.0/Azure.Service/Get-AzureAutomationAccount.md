---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006577"
---
# <span data-ttu-id="b776a-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b776a-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="b776a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b776a-102">SYNOPSIS</span></span>

<span data-ttu-id="b776a-103">Ruft Azure Automation-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="b776a-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="b776a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b776a-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b776a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b776a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b776a-106">Das Cmdlet " **Get-AzureAutomationAccount** " Ruft die Microsoft Azure Automation-Konten für Ihr Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b776a-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="b776a-107">Bei einem Automatisierungs Konto handelt es sich um einen Container für Automatisierungs Ressourcen, der von den Ressourcen anderer Automatisierungs Konten isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="b776a-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="b776a-108">Automatisierungs Ressourcen umfassen runbooks, Aufträge und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b776a-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="b776a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b776a-109">EXAMPLES</span></span>

### <span data-ttu-id="b776a-110">Beispiel 1: Abrufen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="b776a-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="b776a-111">Dieser Befehl ruft das Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="b776a-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b776a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b776a-112">PARAMETERS</span></span>

### <span data-ttu-id="b776a-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="b776a-113">-Location</span></span>
<span data-ttu-id="b776a-114">Gibt eine Azure-Position an, die Automatisierungs Konten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b776a-114">Specifies an Azure location associated with Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b776a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b776a-115">-Name</span></span>
<span data-ttu-id="b776a-116">Gibt den Namen eines Azure Automation-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b776a-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b776a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="b776a-117">-Profile</span></span>
<span data-ttu-id="b776a-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b776a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b776a-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b776a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b776a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b776a-120">CommonParameters</span></span>
<span data-ttu-id="b776a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b776a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b776a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b776a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b776a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b776a-123">INPUTS</span></span>

## <span data-ttu-id="b776a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b776a-124">OUTPUTS</span></span>

### <span data-ttu-id="b776a-125">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b776a-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="b776a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b776a-126">NOTES</span></span>

## <span data-ttu-id="b776a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b776a-127">RELATED LINKS</span></span>

[<span data-ttu-id="b776a-128">Neu – AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b776a-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="b776a-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b776a-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


