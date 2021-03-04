---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: d06f8b5efa0a220b20c5324b457a870d5aaa44b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933144"
---
# <span data-ttu-id="34848-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="34848-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="34848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34848-102">SYNOPSIS</span></span>
<span data-ttu-id="34848-103">Ruft eine RDP-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="34848-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="34848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34848-104">SYNTAX</span></span>

### <span data-ttu-id="34848-105">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="34848-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34848-106">Starten</span><span class="sxs-lookup"><span data-stu-id="34848-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34848-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34848-107">DESCRIPTION</span></span>
<span data-ttu-id="34848-108">Das **Get-AzRemoteDesktopFile-Cmdlet** ruft eine Remotedesktopprotokolldatei (RDP) ab.</span><span class="sxs-lookup"><span data-stu-id="34848-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="34848-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34848-109">EXAMPLES</span></span>

### <span data-ttu-id="34848-110">Beispiel 1: Herunterladen einer Remotedesktopdatei</span><span class="sxs-lookup"><span data-stu-id="34848-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="34848-111">Dieser Befehl ruft die Remotedesktopdatei für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="34848-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="34848-112">Der Befehl speichert das Ergebnis in der Datei "D:\RemoteDesktopFile07.rdp".</span><span class="sxs-lookup"><span data-stu-id="34848-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="34848-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="34848-113">PARAMETERS</span></span>

### <span data-ttu-id="34848-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34848-114">-DefaultProfile</span></span>
<span data-ttu-id="34848-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34848-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34848-116">-Start</span><span class="sxs-lookup"><span data-stu-id="34848-116">-Launch</span></span>
<span data-ttu-id="34848-117">Gibt an, dass dieses Cmdlet Remotedesktop startet, nachdem es die RDP-Datei erhält.</span><span class="sxs-lookup"><span data-stu-id="34848-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34848-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="34848-118">-LocalPath</span></span>
<span data-ttu-id="34848-119">Gibt den lokalen vollständigen Pfad an, in dem dieses Cmdlet die RDP-Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="34848-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34848-120">-Name</span><span class="sxs-lookup"><span data-stu-id="34848-120">-Name</span></span>
<span data-ttu-id="34848-121">Gibt den Namen des Verfügbarkeitssets an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="34848-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34848-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34848-122">-ResourceGroupName</span></span>
<span data-ttu-id="34848-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="34848-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34848-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34848-124">CommonParameters</span></span>
<span data-ttu-id="34848-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34848-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34848-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34848-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34848-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34848-127">INPUTS</span></span>

### <span data-ttu-id="34848-128">System.String</span><span class="sxs-lookup"><span data-stu-id="34848-128">System.String</span></span>

## <span data-ttu-id="34848-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34848-129">OUTPUTS</span></span>

### <span data-ttu-id="34848-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="34848-130">System.Void</span></span>

## <span data-ttu-id="34848-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="34848-131">NOTES</span></span>

## <span data-ttu-id="34848-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="34848-132">RELATED LINKS</span></span>
