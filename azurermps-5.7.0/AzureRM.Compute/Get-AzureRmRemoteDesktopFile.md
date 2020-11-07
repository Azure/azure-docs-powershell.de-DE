---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662963"
---
# <span data-ttu-id="60cd5-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="60cd5-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="60cd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="60cd5-103">Ruft eine RDP-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="60cd5-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60cd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60cd5-104">SYNTAX</span></span>

### <span data-ttu-id="60cd5-105">Download</span><span class="sxs-lookup"><span data-stu-id="60cd5-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="60cd5-106">Starten</span><span class="sxs-lookup"><span data-stu-id="60cd5-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="60cd5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60cd5-107">DESCRIPTION</span></span>
<span data-ttu-id="60cd5-108">Das Cmdlet " **Get-AzureRmRemoteDesktopFile** " Ruft eine RDP-Datei (Remote Desktop Protocol) ab.</span><span class="sxs-lookup"><span data-stu-id="60cd5-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="60cd5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60cd5-109">EXAMPLES</span></span>

### <span data-ttu-id="60cd5-110">Beispiel 1: Abrufen einer Remote Desktop Datei</span><span class="sxs-lookup"><span data-stu-id="60cd5-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="60cd5-111">Dieser Befehl ruft die Remote Desktop Datei für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="60cd5-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="60cd5-112">Der Befehl speichert das Ergebnis in der Datei mit dem Namen D:\RemoteDesktopFile07.RDP.</span><span class="sxs-lookup"><span data-stu-id="60cd5-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="60cd5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="60cd5-113">PARAMETERS</span></span>

### <span data-ttu-id="60cd5-114">-Start</span><span class="sxs-lookup"><span data-stu-id="60cd5-114">-Launch</span></span>
<span data-ttu-id="60cd5-115">Gibt an, dass dieses Cmdlet den Remote Desktop startet, nachdem die RDP-Datei abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="60cd5-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cd5-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="60cd5-116">-LocalPath</span></span>
<span data-ttu-id="60cd5-117">Gibt den lokalen vollständigen Pfad an, in dem dieses Cmdlet die RDP-Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="60cd5-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60cd5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="60cd5-118">-Name</span></span>
<span data-ttu-id="60cd5-119">Gibt den Namen des Verfügbarkeits Satzes an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="60cd5-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60cd5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cd5-120">-ResourceGroupName</span></span>
<span data-ttu-id="60cd5-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="60cd5-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="60cd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cd5-122">CommonParameters</span></span>
<span data-ttu-id="60cd5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cd5-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60cd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cd5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60cd5-125">INPUTS</span></span>

### <span data-ttu-id="60cd5-126">Keine</span><span class="sxs-lookup"><span data-stu-id="60cd5-126">None</span></span>
<span data-ttu-id="60cd5-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="60cd5-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60cd5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60cd5-128">OUTPUTS</span></span>

## <span data-ttu-id="60cd5-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="60cd5-129">NOTES</span></span>

## <span data-ttu-id="60cd5-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60cd5-130">RELATED LINKS</span></span>

