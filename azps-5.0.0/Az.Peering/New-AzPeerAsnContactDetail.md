---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176575"
---
# <span data-ttu-id="42e1a-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="42e1a-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="42e1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="42e1a-103">Erstellt eine in-Memory-Kontakt Detail für PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="42e1a-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="42e1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42e1a-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="42e1a-106">Erstellen eines in-Memory-PeerAsn-Kontaktdetails</span><span class="sxs-lookup"><span data-stu-id="42e1a-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="42e1a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="42e1a-108">Kontaktdetails erstellen und zu PeerAsn hinzufügen</span><span class="sxs-lookup"><span data-stu-id="42e1a-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="42e1a-109">Rolle und e-Mail sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42e1a-109">Role and email are required.</span></span> <span data-ttu-id="42e1a-110">Telefon ist optional.</span><span class="sxs-lookup"><span data-stu-id="42e1a-110">Phone is optional.</span></span> <span data-ttu-id="42e1a-111">Telefon unterstützt +-() oder Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="42e1a-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="42e1a-112">Ein PeerAsn muss mindestens ein Kontakt Detail des Typs "NOC" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="42e1a-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="42e1a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="42e1a-113">PARAMETERS</span></span>

### <span data-ttu-id="42e1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e1a-114">-DefaultProfile</span></span>
<span data-ttu-id="42e1a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42e1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e1a-116">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="42e1a-116">-Email</span></span>
<span data-ttu-id="42e1a-117">E-Mail-Adressen, die für die Kontaktaufnahme verwendet werden, wenn Probleme arrise in der Regel ein Netzwerk</span><span class="sxs-lookup"><span data-stu-id="42e1a-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="42e1a-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="42e1a-118">-Phone</span></span>
<span data-ttu-id="42e1a-119">Telefon, das für die Kontaktaufnahme verwendet wird, wenn Probleme arrise in der Regel ein Netzwerkbetriebs Center</span><span class="sxs-lookup"><span data-stu-id="42e1a-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="42e1a-120">-Role</span><span class="sxs-lookup"><span data-stu-id="42e1a-120">-Role</span></span>
<span data-ttu-id="42e1a-121">Wählen Sie die Rolle aus, die für die Kontaktinformationen am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="42e1a-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="42e1a-122">NOC-Kontakt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42e1a-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="42e1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e1a-123">CommonParameters</span></span>
<span data-ttu-id="42e1a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e1a-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42e1a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e1a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42e1a-126">INPUTS</span></span>

### <span data-ttu-id="42e1a-127">Keine</span><span class="sxs-lookup"><span data-stu-id="42e1a-127">None</span></span>

## <span data-ttu-id="42e1a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42e1a-128">OUTPUTS</span></span>

### <span data-ttu-id="42e1a-129">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="42e1a-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="42e1a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="42e1a-130">NOTES</span></span>

## <span data-ttu-id="42e1a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42e1a-131">RELATED LINKS</span></span>
