---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006441"
---
# <span data-ttu-id="9039b-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="9039b-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="9039b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9039b-102">SYNOPSIS</span></span>
<span data-ttu-id="9039b-103">Erstellt ein leeres ACL-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="9039b-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="9039b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9039b-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9039b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9039b-105">DESCRIPTION</span></span>
<span data-ttu-id="9039b-106">Mit dem Cmdlet **New-AzureAclConfig** wird ein leeres Konfigurationsobjekt für die Zugriffssteuerungsliste (ACL) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9039b-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="9039b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9039b-107">EXAMPLES</span></span>

### <span data-ttu-id="9039b-108">Beispiel 1: Erstellen eines ACL-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="9039b-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="9039b-109">Dieser Befehl erstellt ein leeres ACL-Konfigurationsobjekt und speichert es dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9039b-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="9039b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9039b-110">PARAMETERS</span></span>

### <span data-ttu-id="9039b-111">-Information</span><span class="sxs-lookup"><span data-stu-id="9039b-111">-InformationAction</span></span>
<span data-ttu-id="9039b-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9039b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9039b-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9039b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9039b-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9039b-114">Continue</span></span>
- <span data-ttu-id="9039b-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9039b-115">Ignore</span></span>
- <span data-ttu-id="9039b-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9039b-116">Inquire</span></span>
- <span data-ttu-id="9039b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9039b-117">SilentlyContinue</span></span>
- <span data-ttu-id="9039b-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="9039b-118">Stop</span></span>
- <span data-ttu-id="9039b-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9039b-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9039b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9039b-120">-InformationVariable</span></span>
<span data-ttu-id="9039b-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9039b-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9039b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9039b-122">CommonParameters</span></span>
<span data-ttu-id="9039b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9039b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9039b-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9039b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9039b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9039b-125">INPUTS</span></span>

## <span data-ttu-id="9039b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9039b-126">OUTPUTS</span></span>

## <span data-ttu-id="9039b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9039b-127">NOTES</span></span>

## <span data-ttu-id="9039b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9039b-128">RELATED LINKS</span></span>

[<span data-ttu-id="9039b-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="9039b-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="9039b-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="9039b-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="9039b-131">Satz-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="9039b-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


