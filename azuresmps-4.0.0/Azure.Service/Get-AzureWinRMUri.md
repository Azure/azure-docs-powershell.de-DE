---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006711"
---
# <span data-ttu-id="5a544-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="5a544-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="5a544-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a544-102">SYNOPSIS</span></span>
<span data-ttu-id="5a544-103">Ruft den URI für WinRM-HTTPS-Listener zu einem virtuellen Computer oder eine Liste virtueller Computer in einem gehosteten Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="5a544-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="5a544-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a544-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5a544-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a544-105">DESCRIPTION</span></span>
<span data-ttu-id="5a544-106">Das Cmdlet " **Get-AzureWinRMUri** " Ruft den URI des Windows Remote Management (WinRM)-HTTPS-Listener zu einem virtuellen Computer oder eine Liste mit virtuellen Computern in einem gehosteten Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="5a544-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="5a544-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a544-107">EXAMPLES</span></span>

### <span data-ttu-id="5a544-108">Beispiel 1: Abrufen des URIs des WinRM-HTTPS-Listener zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="5a544-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="5a544-109">Dieser Befehl ruft die UIR des WinRM-HTTPS-Listener zu einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="5a544-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="5a544-110">Beispiel 2: Abrufen des URIs des WinRM-HTTPS-Listener zu einem virtuellen Computer eines bestimmten Diensts</span><span class="sxs-lookup"><span data-stu-id="5a544-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="5a544-111">Dieser Befehl ruft die UIR des WinRM-HTTPS-Listener zu einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="5a544-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="5a544-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a544-112">PARAMETERS</span></span>

### <span data-ttu-id="5a544-113">-Information</span><span class="sxs-lookup"><span data-stu-id="5a544-113">-InformationAction</span></span>
<span data-ttu-id="5a544-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5a544-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5a544-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5a544-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a544-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5a544-116">Continue</span></span>
- <span data-ttu-id="5a544-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5a544-117">Ignore</span></span>
- <span data-ttu-id="5a544-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5a544-118">Inquire</span></span>
- <span data-ttu-id="5a544-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5a544-119">SilentlyContinue</span></span>
- <span data-ttu-id="5a544-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="5a544-120">Stop</span></span>
- <span data-ttu-id="5a544-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5a544-121">Suspend</span></span>

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

### <span data-ttu-id="5a544-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5a544-122">-InformationVariable</span></span>
<span data-ttu-id="5a544-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5a544-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5a544-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5a544-124">-Name</span></span>
<span data-ttu-id="5a544-125">Gibt den Namen des virtuellen Computers an, auf den der WinRM-URI generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a544-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a544-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="5a544-126">-Profile</span></span>
<span data-ttu-id="5a544-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5a544-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a544-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5a544-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a544-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5a544-129">-ServiceName</span></span>
<span data-ttu-id="5a544-130">Gibt den Namen des Microsoft Azure-Diensts an, der den virtuellen Computer hostet.</span><span class="sxs-lookup"><span data-stu-id="5a544-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a544-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a544-131">CommonParameters</span></span>
<span data-ttu-id="5a544-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a544-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a544-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a544-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a544-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a544-134">INPUTS</span></span>

## <span data-ttu-id="5a544-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a544-135">OUTPUTS</span></span>

## <span data-ttu-id="5a544-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a544-136">NOTES</span></span>

## <span data-ttu-id="5a544-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a544-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a544-138">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="5a544-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="5a544-139">Neu – AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="5a544-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


