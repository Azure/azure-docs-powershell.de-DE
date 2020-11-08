---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006202"
---
# <span data-ttu-id="c34f9-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c34f9-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="c34f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c34f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c34f9-103">Erstellt eine Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="c34f9-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c34f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c34f9-104">SYNTAX</span></span>

### <span data-ttu-id="c34f9-105">AllParameterSets (Standard)</span><span class="sxs-lookup"><span data-stu-id="c34f9-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c34f9-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="c34f9-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c34f9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c34f9-107">DESCRIPTION</span></span>
<span data-ttu-id="c34f9-108">Das Cmdlet **New-AzureRemoteAppCollection** erstellt eine Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="c34f9-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c34f9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c34f9-109">EXAMPLES</span></span>

### <span data-ttu-id="c34f9-110">Beispiel 1: Erstellen einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="c34f9-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="c34f9-111">Dieser Befehl erstellt eine Azure RemoteApp-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="c34f9-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="c34f9-112">Beispiel 2: Erstellen einer Sammlung mithilfe von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="c34f9-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="c34f9-113">Dieser Befehl erstellt eine Azure RemoteApp-Sammlung unter Verwendung einer Anmeldeinformationen aus dem Cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="c34f9-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="c34f9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c34f9-114">PARAMETERS</span></span>

### <span data-ttu-id="c34f9-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="c34f9-115">-CollectionName</span></span>
<span data-ttu-id="c34f9-116">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-116">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="c34f9-117">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="c34f9-117">-Credential</span></span>
<span data-ttu-id="c34f9-118">Gibt die Anmeldeinformationen eines Dienstkontos an, das über die Berechtigung zum beitreten der Azure RemoteApp-Server zu Ihrer Domäne verfügt.</span><span class="sxs-lookup"><span data-stu-id="c34f9-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="c34f9-119">Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c34f9-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="c34f9-120">-CustomRdpProperty</span></span>
<span data-ttu-id="c34f9-121">Gibt benutzerdefinierte Remote Desktop-Eigenschaften an, die zum Konfigurieren der Laufwerkumleitung und anderer Einstellungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c34f9-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="c34f9-122">Details finden Sie unter [RDP-Einstellungen für Remote Desktop Dienste in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="c34f9-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

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

### <span data-ttu-id="c34f9-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c34f9-123">-Description</span></span>
<span data-ttu-id="c34f9-124">Gibt eine kurze Beschreibung für das Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-124">Specifies a short description for the object.</span></span>

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

### <span data-ttu-id="c34f9-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="c34f9-125">-DnsServers</span></span>
<span data-ttu-id="c34f9-126">Gibt eine durch trennzeichengetrennte Liste der IPv4-Adressen der DNS-Server an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-127">-Domäne</span><span class="sxs-lookup"><span data-stu-id="c34f9-127">-Domain</span></span>
<span data-ttu-id="c34f9-128">Gibt den Namen der Active Directory-Domänendienst Domäne an, an die die Server mit dem Host für Remotedesktopsitzungen teilnehmen sollen.</span><span class="sxs-lookup"><span data-stu-id="c34f9-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-129">-Bildname</span><span class="sxs-lookup"><span data-stu-id="c34f9-129">-ImageName</span></span>
<span data-ttu-id="c34f9-130">Gibt den Namen des Azure RemoteApp-Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="c34f9-131">-Location</span></span>
<span data-ttu-id="c34f9-132">Gibt den Azure-Bereich der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="c34f9-133">-OrganizationalUnit</span></span>
<span data-ttu-id="c34f9-134">Gibt den Namen der Organisationseinheit an, an die die Hostserver für Remotedesktopsitzungen teilnehmen sollen, beispielsweise ou = MyOu, DC = MyDomain, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="c34f9-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="c34f9-135">Attribute wie ou und DC müssen in Großbuchstaben eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c34f9-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="c34f9-136">Die OU kann nach der Erstellung der Sammlung nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c34f9-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-137">-Plan</span><span class="sxs-lookup"><span data-stu-id="c34f9-137">-Plan</span></span>
<span data-ttu-id="c34f9-138">Gibt den Plan für die Azure RemoteApp-Sammlung an, die die Nutzungs Grenzwerte definieren kann.</span><span class="sxs-lookup"><span data-stu-id="c34f9-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="c34f9-139">Verwenden Sie " **Get-AzureRemoteAppPlan** ", um die verfügbaren Pläne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c34f9-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="c34f9-140">-Profile</span></span>
<span data-ttu-id="c34f9-141">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c34f9-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c34f9-142">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c34f9-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c34f9-143">-</span><span class="sxs-lookup"><span data-stu-id="c34f9-143">-ResourceType</span></span>
<span data-ttu-id="c34f9-144">Gibt den Ressourcentyp der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="c34f9-145">Die akzeptablen Werte für diesen Parameter sind: App oder Desktop.</span><span class="sxs-lookup"><span data-stu-id="c34f9-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c34f9-146">-SubnetName</span></span>
<span data-ttu-id="c34f9-147">Gibt den Namen des Subnets im virtuellen Netzwerk an, das zum Erstellen der Azure RemoteApp-Sammlung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c34f9-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c34f9-148">-VNetName</span></span>
<span data-ttu-id="c34f9-149">Gibt den Namen eines virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="c34f9-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34f9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34f9-150">CommonParameters</span></span>
<span data-ttu-id="c34f9-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c34f9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34f9-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34f9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34f9-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c34f9-153">INPUTS</span></span>

## <span data-ttu-id="c34f9-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c34f9-154">OUTPUTS</span></span>

## <span data-ttu-id="c34f9-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="c34f9-155">NOTES</span></span>

## <span data-ttu-id="c34f9-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c34f9-156">RELATED LINKS</span></span>

[<span data-ttu-id="c34f9-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c34f9-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="c34f9-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="c34f9-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="c34f9-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c34f9-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="c34f9-160">Satz-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c34f9-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="c34f9-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c34f9-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


