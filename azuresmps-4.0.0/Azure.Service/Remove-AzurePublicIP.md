---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006354"
---
# <span data-ttu-id="13258-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="13258-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="13258-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13258-102">SYNOPSIS</span></span>
<span data-ttu-id="13258-103">Entfernt die öffentliche IP-Konfiguration von einem Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="13258-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="13258-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13258-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13258-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13258-105">DESCRIPTION</span></span>
<span data-ttu-id="13258-106">Das Cmdlet **Remove-AzurePublicIP** entfernt die öffentliche IP-Konfiguration von einem Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="13258-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="13258-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13258-107">EXAMPLES</span></span>

### <span data-ttu-id="13258-108">Beispiel 1: Entfernen der öffentlichen IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="13258-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="13258-109">Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="13258-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="13258-110">Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13258-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13258-111">Das aktuelle Cmdlet entfernt die öffentliche IP-Konfiguration vom virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="13258-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="13258-112">Der Befehl übergibt den virtuellen Computer an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="13258-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="13258-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="13258-113">PARAMETERS</span></span>

### <span data-ttu-id="13258-114">-Information</span><span class="sxs-lookup"><span data-stu-id="13258-114">-InformationAction</span></span>
<span data-ttu-id="13258-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="13258-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13258-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="13258-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13258-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="13258-117">Continue</span></span>
- <span data-ttu-id="13258-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="13258-118">Ignore</span></span>
- <span data-ttu-id="13258-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="13258-119">Inquire</span></span>
- <span data-ttu-id="13258-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13258-120">SilentlyContinue</span></span>
- <span data-ttu-id="13258-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="13258-121">Stop</span></span>
- <span data-ttu-id="13258-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="13258-122">Suspend</span></span>

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

### <span data-ttu-id="13258-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13258-123">-InformationVariable</span></span>
<span data-ttu-id="13258-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="13258-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13258-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="13258-125">-Profile</span></span>
<span data-ttu-id="13258-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="13258-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13258-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="13258-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13258-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="13258-128">-PublicIPName</span></span>
<span data-ttu-id="13258-129">Gibt den öffentlichen IP-Namen an.</span><span class="sxs-lookup"><span data-stu-id="13258-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13258-130">-VM</span><span class="sxs-lookup"><span data-stu-id="13258-130">-VM</span></span>
<span data-ttu-id="13258-131">Gibt den virtuellen Computer an, von dem dieses Cmdlet die öffentliche IP-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="13258-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="13258-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13258-132">CommonParameters</span></span>
<span data-ttu-id="13258-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13258-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13258-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13258-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13258-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13258-135">INPUTS</span></span>

## <span data-ttu-id="13258-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13258-136">OUTPUTS</span></span>

### <span data-ttu-id="13258-137">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="13258-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="13258-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="13258-138">NOTES</span></span>

## <span data-ttu-id="13258-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13258-139">RELATED LINKS</span></span>

[<span data-ttu-id="13258-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="13258-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="13258-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="13258-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="13258-142">Satz-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="13258-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="13258-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="13258-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


