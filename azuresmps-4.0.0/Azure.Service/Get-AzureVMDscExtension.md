---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006744"
---
# <span data-ttu-id="2ab30-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2ab30-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="2ab30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ab30-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab30-103">Ruft die Einstellungen der DSC-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2ab30-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="2ab30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ab30-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ab30-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ab30-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab30-106">Das Cmdlet " **Get-AzureVMDscExtension** " Ruft die Einstellungen der DSC-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2ab30-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="2ab30-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ab30-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab30-108">Beispiel 1: Abrufen der Einstellung der DSC-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="2ab30-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="2ab30-109">Dieser Befehl ruft die Einstellungen der DSC-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2ab30-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="2ab30-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ab30-110">PARAMETERS</span></span>

### <span data-ttu-id="2ab30-111">-Information</span><span class="sxs-lookup"><span data-stu-id="2ab30-111">-InformationAction</span></span>
<span data-ttu-id="2ab30-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="2ab30-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ab30-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ab30-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ab30-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="2ab30-114">Continue</span></span>
- <span data-ttu-id="2ab30-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="2ab30-115">Ignore</span></span>
- <span data-ttu-id="2ab30-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="2ab30-116">Inquire</span></span>
- <span data-ttu-id="2ab30-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ab30-117">SilentlyContinue</span></span>
- <span data-ttu-id="2ab30-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="2ab30-118">Stop</span></span>
- <span data-ttu-id="2ab30-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="2ab30-119">Suspend</span></span>

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

### <span data-ttu-id="2ab30-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ab30-120">-InformationVariable</span></span>
<span data-ttu-id="2ab30-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="2ab30-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ab30-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ab30-122">-Profile</span></span>
<span data-ttu-id="2ab30-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2ab30-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ab30-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2ab30-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ab30-125">-VM</span><span class="sxs-lookup"><span data-stu-id="2ab30-125">-VM</span></span>
<span data-ttu-id="2ab30-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2ab30-126">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab30-127">CommonParameters</span></span>
<span data-ttu-id="2ab30-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab30-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab30-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab30-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ab30-130">INPUTS</span></span>

## <span data-ttu-id="2ab30-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ab30-131">OUTPUTS</span></span>

### <span data-ttu-id="2ab30-132">Microsoft. WindowsAzure. Commands. Servicemanagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="2ab30-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="2ab30-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ab30-133">NOTES</span></span>

## <span data-ttu-id="2ab30-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ab30-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ab30-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2ab30-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="2ab30-136">Satz-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2ab30-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="2ab30-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="2ab30-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


