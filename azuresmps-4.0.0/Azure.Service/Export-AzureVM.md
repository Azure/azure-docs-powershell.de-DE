---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005883"
---
# <span data-ttu-id="6e784-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6e784-101">Export-AzureVM</span></span>

## <span data-ttu-id="6e784-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e784-102">SYNOPSIS</span></span>
<span data-ttu-id="6e784-103">Exportiert einen Zustand des Azure Virtual Machine in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="6e784-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="6e784-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e784-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6e784-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e784-105">DESCRIPTION</span></span>
<span data-ttu-id="6e784-106">Das Cmdlet **Export-AzureVM** exportiert den Zustand einer virtuellen Maschine in eine XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="6e784-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="6e784-107">Beim Ausführen von " **Export-AzureVM** ", gefolgt von " **Remove-AzureVM** " und dann " **Import-AzureVM** ", um einen virtuellen Computer neu zu erstellen, kann die resultierende virtuelle Maschine eine andere IP-Adresse als das Original aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6e784-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="6e784-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e784-108">EXAMPLES</span></span>

### <span data-ttu-id="6e784-109">Beispiel 1: Exportieren eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="6e784-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="6e784-110">Dieser Befehl exportiert den Zustand des angegebenen virtuellen Computers in die VMstate.xml-Datei.</span><span class="sxs-lookup"><span data-stu-id="6e784-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="6e784-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e784-111">PARAMETERS</span></span>

### <span data-ttu-id="6e784-112">-Information</span><span class="sxs-lookup"><span data-stu-id="6e784-112">-InformationAction</span></span>
<span data-ttu-id="6e784-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6e784-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6e784-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6e784-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e784-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6e784-115">Continue</span></span>
- <span data-ttu-id="6e784-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6e784-116">Ignore</span></span>
- <span data-ttu-id="6e784-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6e784-117">Inquire</span></span>
- <span data-ttu-id="6e784-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6e784-118">SilentlyContinue</span></span>
- <span data-ttu-id="6e784-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="6e784-119">Stop</span></span>
- <span data-ttu-id="6e784-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6e784-120">Suspend</span></span>

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

### <span data-ttu-id="6e784-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6e784-121">-InformationVariable</span></span>
<span data-ttu-id="6e784-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6e784-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6e784-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6e784-123">-Name</span></span>
<span data-ttu-id="6e784-124">Gibt den Namen des virtuellen Computers an, für den das Cmdlet den Zustand exportiert.</span><span class="sxs-lookup"><span data-stu-id="6e784-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e784-125">-Path</span><span class="sxs-lookup"><span data-stu-id="6e784-125">-Path</span></span>
<span data-ttu-id="6e784-126">Gibt den Pfad und den Dateinamen an, zu dem dieses Cmdlet den Zustand des virtuellen Computers speichert.</span><span class="sxs-lookup"><span data-stu-id="6e784-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

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

### <span data-ttu-id="6e784-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e784-127">-Profile</span></span>
<span data-ttu-id="6e784-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6e784-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e784-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6e784-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e784-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6e784-130">-ServiceName</span></span>
<span data-ttu-id="6e784-131">Gibt den Namen des Azure-Diensts an, der den virtuellen Computer hostet.</span><span class="sxs-lookup"><span data-stu-id="6e784-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="6e784-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e784-132">CommonParameters</span></span>
<span data-ttu-id="6e784-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e784-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e784-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e784-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e784-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e784-135">INPUTS</span></span>

## <span data-ttu-id="6e784-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e784-136">OUTPUTS</span></span>

## <span data-ttu-id="6e784-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e784-137">NOTES</span></span>

## <span data-ttu-id="6e784-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e784-138">RELATED LINKS</span></span>

[<span data-ttu-id="6e784-139">Importieren-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6e784-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


