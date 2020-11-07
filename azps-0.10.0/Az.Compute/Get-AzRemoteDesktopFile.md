---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 413977ee42b0edc2221cbbdcfd34b6130d40f74e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844647"
---
# <span data-ttu-id="ada3c-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="ada3c-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="ada3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ada3c-102">SYNOPSIS</span></span>
<span data-ttu-id="ada3c-103">Ruft eine RDP-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="ada3c-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="ada3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ada3c-104">SYNTAX</span></span>

### <span data-ttu-id="ada3c-105">Download</span><span class="sxs-lookup"><span data-stu-id="ada3c-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ada3c-106">Starten</span><span class="sxs-lookup"><span data-stu-id="ada3c-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada3c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ada3c-107">DESCRIPTION</span></span>
<span data-ttu-id="ada3c-108">Das Cmdlet " **Get-AzRemoteDesktopFile** " Ruft eine RDP-Datei (Remote Desktop Protocol) ab.</span><span class="sxs-lookup"><span data-stu-id="ada3c-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="ada3c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ada3c-109">EXAMPLES</span></span>

### <span data-ttu-id="ada3c-110">Beispiel 1: Abrufen einer Remote Desktop Datei</span><span class="sxs-lookup"><span data-stu-id="ada3c-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="ada3c-111">Dieser Befehl ruft die Remote Desktop Datei für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="ada3c-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ada3c-112">Der Befehl speichert das Ergebnis in der Datei mit dem Namen D:\RemoteDesktopFile07.RDP.</span><span class="sxs-lookup"><span data-stu-id="ada3c-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="ada3c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ada3c-113">PARAMETERS</span></span>

### <span data-ttu-id="ada3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada3c-114">-DefaultProfile</span></span>
<span data-ttu-id="ada3c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ada3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada3c-116">-Start</span><span class="sxs-lookup"><span data-stu-id="ada3c-116">-Launch</span></span>
<span data-ttu-id="ada3c-117">Gibt an, dass dieses Cmdlet den Remote Desktop startet, nachdem die RDP-Datei abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ada3c-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="ada3c-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ada3c-118">-LocalPath</span></span>
<span data-ttu-id="ada3c-119">Gibt den lokalen vollständigen Pfad an, in dem dieses Cmdlet die RDP-Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="ada3c-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="ada3c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ada3c-120">-Name</span></span>
<span data-ttu-id="ada3c-121">Gibt den Namen des Verfügbarkeits Satzes an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ada3c-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ada3c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada3c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ada3c-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ada3c-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ada3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada3c-124">CommonParameters</span></span>
<span data-ttu-id="ada3c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada3c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada3c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada3c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ada3c-127">INPUTS</span></span>

### <span data-ttu-id="ada3c-128">Keine</span><span class="sxs-lookup"><span data-stu-id="ada3c-128">None</span></span>
<span data-ttu-id="ada3c-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ada3c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ada3c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ada3c-130">OUTPUTS</span></span>

## <span data-ttu-id="ada3c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ada3c-131">NOTES</span></span>

## <span data-ttu-id="ada3c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ada3c-132">RELATED LINKS</span></span>

