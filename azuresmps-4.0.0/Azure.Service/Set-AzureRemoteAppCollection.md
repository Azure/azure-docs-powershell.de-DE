---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006259"
---
# <span data-ttu-id="f75c3-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f75c3-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="f75c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f75c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f75c3-103">Legt die Eigenschaften einer RemoteApp-Sammlung fest.</span><span class="sxs-lookup"><span data-stu-id="f75c3-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="f75c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f75c3-104">SYNTAX</span></span>

### <span data-ttu-id="f75c3-105">DescriptionOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="f75c3-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f75c3-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="f75c3-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f75c3-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="f75c3-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f75c3-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="f75c3-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f75c3-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="f75c3-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f75c3-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f75c3-110">DESCRIPTION</span></span>
<span data-ttu-id="f75c3-111">Mit dem Cmdlet **Set-AzureRemoteAppCollection** werden die Eigenschaften einer Azure RemoteApp-Sammlung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f75c3-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f75c3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f75c3-112">EXAMPLES</span></span>

## <span data-ttu-id="f75c3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f75c3-113">PARAMETERS</span></span>

### <span data-ttu-id="f75c3-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="f75c3-114">-AclLevel</span></span>
<span data-ttu-id="f75c3-115">Gibt die Zugriffssteuerungslisten Ebene für die Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="f75c3-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="f75c3-116">Die akzeptablen Werte für diesen Parameter sind: Sammlung und Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f75c3-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c3-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f75c3-117">-CollectionName</span></span>
<span data-ttu-id="f75c3-118">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="f75c3-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c3-119">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f75c3-119">-Credential</span></span>
<span data-ttu-id="f75c3-120">Gibt die Anmeldeinformationen eines Dienstkontos an, das über die Berechtigung zum beitreten der Azure RemoteApp-Server zu Ihrer Domäne verfügt.</span><span class="sxs-lookup"><span data-stu-id="f75c3-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="f75c3-121">Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f75c3-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c3-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="f75c3-122">-CustomRdpProperty</span></span>
<span data-ttu-id="f75c3-123">Gibt benutzerdefinierte RDP-Eigenschaften (Remote Desktop Protocol) an, die zum Konfigurieren der Laufwerkumleitung und anderer Einstellungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f75c3-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="f75c3-124">Details finden Sie unter [RDP-Einstellungen für Remote Desktop Dienste in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="f75c3-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c3-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f75c3-125">-Description</span></span>
<span data-ttu-id="f75c3-126">Gibt eine kurze Beschreibung für die Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="f75c3-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c3-127">-Plan</span><span class="sxs-lookup"><span data-stu-id="f75c3-127">-Plan</span></span>
<span data-ttu-id="f75c3-128">Gibt den Plan für die Azure RemoteApp-Sammlung an, die die Nutzungs Grenzwerte definiert.</span><span class="sxs-lookup"><span data-stu-id="f75c3-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="f75c3-129">Verwenden Sie " **Get-AzureRemoteAppPlan** ", um die verfügbaren Pläne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f75c3-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c3-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="f75c3-130">-Profile</span></span>
<span data-ttu-id="f75c3-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f75c3-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f75c3-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f75c3-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f75c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75c3-133">CommonParameters</span></span>
<span data-ttu-id="f75c3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75c3-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75c3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f75c3-136">INPUTS</span></span>

## <span data-ttu-id="f75c3-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f75c3-137">OUTPUTS</span></span>

## <span data-ttu-id="f75c3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f75c3-138">NOTES</span></span>

## <span data-ttu-id="f75c3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f75c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="f75c3-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f75c3-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="f75c3-141">Neu – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f75c3-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="f75c3-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f75c3-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


