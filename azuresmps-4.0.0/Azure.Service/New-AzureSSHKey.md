---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006188"
---
# <span data-ttu-id="78a08-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="78a08-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="78a08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78a08-102">SYNOPSIS</span></span>
<span data-ttu-id="78a08-103">Erstellt ein SSH-Schlüsselobjekt zum Einfügen eines vorhandenen Zertifikats in einen neuen Linux-basierten Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="78a08-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="78a08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78a08-104">SYNTAX</span></span>

### <span data-ttu-id="78a08-105">keyPair</span><span class="sxs-lookup"><span data-stu-id="78a08-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="78a08-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="78a08-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="78a08-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78a08-107">DESCRIPTION</span></span>
<span data-ttu-id="78a08-108">Das Cmdlet **New-AzureSSHKey** erstellt ein SSH-Schlüsselobjekt für ein Zertifikat, das bereits zu Azure hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="78a08-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="78a08-109">Dieses SSH-Schlüsselobjekt kann dann von **New-AzureProvisioningConfig** verwendet werden, wenn das Konfigurationsobjekt für einen neuen virtuellen Computer mithilfe von **New-AzureVM** oder beim Erstellen eines neuen virtuellen Computers mit **New-AzureQuickVM** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="78a08-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="78a08-110">Wenn Sie als Teil eines Skripts für die Erstellung virtueller Maschinen enthalten sind, wird dem neuen virtuellen Computer der angegebene SSH-öffentlicher Schlüssel oder Schlüsselpaar hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78a08-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="78a08-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78a08-111">EXAMPLES</span></span>

### <span data-ttu-id="78a08-112">Beispiel 1: Erstellen eines Zertifikats Einstellungs Objekts</span><span class="sxs-lookup"><span data-stu-id="78a08-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="78a08-113">Dieser Befehl erstellt ein Zertifikat Einstellungsobjekt für ein vorhandenes Zertifikat und speichert das Objekt dann zur späteren Verwendung in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="78a08-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="78a08-114">Beispiel 2: Hinzufügen eines Zertifikats zu einem Dienst</span><span class="sxs-lookup"><span data-stu-id="78a08-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="78a08-115">Dieser Befehl fügt einem Azure-Dienst ein Zertifikat hinzu und erstellt dann einen neuen virtuellen Linux-Computer, der das Zertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="78a08-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="78a08-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="78a08-116">PARAMETERS</span></span>

### <span data-ttu-id="78a08-117">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="78a08-117">-Fingerprint</span></span>
<span data-ttu-id="78a08-118">Gibt den Fingerabdruck des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="78a08-118">Specifies the fingerprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a08-119">-Information</span><span class="sxs-lookup"><span data-stu-id="78a08-119">-InformationAction</span></span>
<span data-ttu-id="78a08-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="78a08-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="78a08-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="78a08-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78a08-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="78a08-122">Continue</span></span>
- <span data-ttu-id="78a08-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="78a08-123">Ignore</span></span>
- <span data-ttu-id="78a08-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="78a08-124">Inquire</span></span>
- <span data-ttu-id="78a08-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="78a08-125">SilentlyContinue</span></span>
- <span data-ttu-id="78a08-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="78a08-126">Stop</span></span>
- <span data-ttu-id="78a08-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="78a08-127">Suspend</span></span>

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

### <span data-ttu-id="78a08-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="78a08-128">-InformationVariable</span></span>
<span data-ttu-id="78a08-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="78a08-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="78a08-130">-KeyPair</span><span class="sxs-lookup"><span data-stu-id="78a08-130">-KeyPair</span></span>
<span data-ttu-id="78a08-131">Gibt an, dass dieses Cmdlet ein Objekt zum Einfügen eines SSH-Schlüsselpaars in die neue Konfiguration des virtuellen Computers erstellt.</span><span class="sxs-lookup"><span data-stu-id="78a08-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a08-132">-Path</span><span class="sxs-lookup"><span data-stu-id="78a08-132">-Path</span></span>
<span data-ttu-id="78a08-133">Gibt den Pfad zum Speichern des öffentlichen SSH-Schlüssels oder Schlüsselpaars an.</span><span class="sxs-lookup"><span data-stu-id="78a08-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a08-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="78a08-134">-PublicKey</span></span>
<span data-ttu-id="78a08-135">Gibt an, dass dieses Cmdlet ein Objekt zum Einfügen eines öffentlichen SSH-Schlüssels in die Konfiguration des neuen virtuellen Computers erstellt.</span><span class="sxs-lookup"><span data-stu-id="78a08-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a08-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a08-136">CommonParameters</span></span>
<span data-ttu-id="78a08-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a08-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a08-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a08-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a08-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78a08-139">INPUTS</span></span>

## <span data-ttu-id="78a08-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78a08-140">OUTPUTS</span></span>

## <span data-ttu-id="78a08-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="78a08-141">NOTES</span></span>

## <span data-ttu-id="78a08-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78a08-142">RELATED LINKS</span></span>

[<span data-ttu-id="78a08-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="78a08-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="78a08-144">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="78a08-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="78a08-145">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="78a08-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="78a08-146">Neu – AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="78a08-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


