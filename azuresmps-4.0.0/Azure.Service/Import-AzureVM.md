---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006461"
---
# <span data-ttu-id="4d6e5-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4d6e5-101">Import-AzureVM</span></span>

## <span data-ttu-id="4d6e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6e5-103">Importiert einen Azure Virtual Machine-Zustand aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="4d6e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d6e5-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d6e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d6e5-105">DESCRIPTION</span></span>
<span data-ttu-id="4d6e5-106">Mit dem Cmdlet " **Import-AzureVM** " wird der zuvor gespeicherte Zustand eines virtuellen Computers aus einer XML-Datei importiert.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="4d6e5-107">Dieses Cmdlet ist nützlich, wenn Sie anschließend einen virtuellen Computer aus den importierten Daten erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="4d6e5-108">Beim Ausführen von " **Export-AzureVM** ", gefolgt von " **Remove-AzureVM** " und dann " **Import-AzureVM** ", um einen virtuellen Computer neu zu erstellen, kann die resultierende virtuelle Maschine eine andere IP-Adresse als das Original aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="4d6e5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d6e5-109">EXAMPLES</span></span>

### <span data-ttu-id="4d6e5-110">Beispiel 1: Importieren eines Zustands eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="4d6e5-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="4d6e5-111">Dieser Befehl importiert den Zustand einer virtuellen Maschine aus der VMstate.xml-Datei und erstellt dann einen virtuellen Computer im angegebenen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="4d6e5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d6e5-112">PARAMETERS</span></span>

### <span data-ttu-id="4d6e5-113">-Information</span><span class="sxs-lookup"><span data-stu-id="4d6e5-113">-InformationAction</span></span>
<span data-ttu-id="4d6e5-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4d6e5-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4d6e5-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d6e5-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4d6e5-116">Continue</span></span>
- <span data-ttu-id="4d6e5-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4d6e5-117">Ignore</span></span>
- <span data-ttu-id="4d6e5-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4d6e5-118">Inquire</span></span>
- <span data-ttu-id="4d6e5-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4d6e5-119">SilentlyContinue</span></span>
- <span data-ttu-id="4d6e5-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="4d6e5-120">Stop</span></span>
- <span data-ttu-id="4d6e5-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4d6e5-121">Suspend</span></span>

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

### <span data-ttu-id="4d6e5-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4d6e5-122">-InformationVariable</span></span>
<span data-ttu-id="4d6e5-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4d6e5-124">-Path</span><span class="sxs-lookup"><span data-stu-id="4d6e5-124">-Path</span></span>
<span data-ttu-id="4d6e5-125">Gibt den Pfad der Datei mit dem Zustand des zuvor gespeicherten virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d6e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6e5-126">CommonParameters</span></span>
<span data-ttu-id="4d6e5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6e5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6e5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6e5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d6e5-129">INPUTS</span></span>

## <span data-ttu-id="4d6e5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d6e5-130">OUTPUTS</span></span>

## <span data-ttu-id="4d6e5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d6e5-131">NOTES</span></span>

## <span data-ttu-id="4d6e5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d6e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="4d6e5-133">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4d6e5-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="4d6e5-134">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="4d6e5-134">New-AzureVM</span></span>](./New-AzureVM.md)


