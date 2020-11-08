---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009605"
---
# <span data-ttu-id="f93b6-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="f93b6-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="f93b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f93b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f93b6-103">Erstellt eine in-Memory-Kontakt Detail für PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="f93b6-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="f93b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f93b6-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f93b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f93b6-105">DESCRIPTION</span></span>
<span data-ttu-id="f93b6-106">Erstellen eines in-Memory-PeerAsn-Kontaktdetails</span><span class="sxs-lookup"><span data-stu-id="f93b6-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="f93b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f93b6-107">EXAMPLES</span></span>

### <span data-ttu-id="f93b6-108">Kontaktdetails erstellen und zu PeerAsn hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f93b6-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="f93b6-109">Rolle und e-Mail sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f93b6-109">Role and email are required.</span></span> <span data-ttu-id="f93b6-110">Telefon ist optional.</span><span class="sxs-lookup"><span data-stu-id="f93b6-110">Phone is optional.</span></span> <span data-ttu-id="f93b6-111">Telefon unterstützt +-() oder Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="f93b6-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="f93b6-112">Ein PeerAsn muss mindestens ein Kontakt Detail des Typs "NOC" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f93b6-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="f93b6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f93b6-113">PARAMETERS</span></span>

### <span data-ttu-id="f93b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93b6-114">-DefaultProfile</span></span>
<span data-ttu-id="f93b6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f93b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f93b6-116">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="f93b6-116">-Email</span></span>
<span data-ttu-id="f93b6-117">E-Mail-Adressen, die für die Kontaktaufnahme verwendet werden, wenn Probleme arrise in der Regel ein Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f93b6-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93b6-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="f93b6-118">-Phone</span></span>
<span data-ttu-id="f93b6-119">Telefon, das für die Kontaktaufnahme verwendet wird, wenn Probleme arrise in der Regel ein Netzwerkbetriebs Center</span><span class="sxs-lookup"><span data-stu-id="f93b6-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93b6-120">-Role</span><span class="sxs-lookup"><span data-stu-id="f93b6-120">-Role</span></span>
<span data-ttu-id="f93b6-121">Wählen Sie die Rolle aus, die für die Kontaktinformationen am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f93b6-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="f93b6-122">NOC-Kontakt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f93b6-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93b6-123">CommonParameters</span></span>
<span data-ttu-id="f93b6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f93b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93b6-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f93b6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93b6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f93b6-126">INPUTS</span></span>

### <span data-ttu-id="f93b6-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f93b6-127">None</span></span>

## <span data-ttu-id="f93b6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f93b6-128">OUTPUTS</span></span>

### <span data-ttu-id="f93b6-129">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="f93b6-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="f93b6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f93b6-130">NOTES</span></span>

## <span data-ttu-id="f93b6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f93b6-131">RELATED LINKS</span></span>
