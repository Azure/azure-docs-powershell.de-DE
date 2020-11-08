---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005902"
---
# <span data-ttu-id="e7745-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="e7745-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="e7745-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7745-102">SYNOPSIS</span></span>
<span data-ttu-id="e7745-103">Deaktiviert den Remote Desktop Zugriff auf einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e7745-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="e7745-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7745-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7745-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7745-105">DESCRIPTION</span></span>
<span data-ttu-id="e7745-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e7745-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e7745-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e7745-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e7745-108">Mit der Funktion " **Disable-AzureServiceProjectRemoteDesktop** " wird der Remotedesktopzugriff auf einen gehosteten Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7745-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="e7745-109">Sie müssen den Dienst mithilfe des Cmdlets **Publish-AzureServiceProject** veröffentlichen, nachdem Sie den Remote Desktop Zugriff deaktiviert haben, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="e7745-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="e7745-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7745-110">EXAMPLES</span></span>

## <span data-ttu-id="e7745-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7745-111">PARAMETERS</span></span>

### <span data-ttu-id="e7745-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7745-112">-PassThru</span></span>
<span data-ttu-id="e7745-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e7745-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7745-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e7745-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7745-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7745-115">-Profile</span></span>
<span data-ttu-id="e7745-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e7745-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7745-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e7745-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7745-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7745-118">CommonParameters</span></span>
<span data-ttu-id="e7745-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7745-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7745-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7745-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7745-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7745-121">INPUTS</span></span>

## <span data-ttu-id="e7745-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7745-122">OUTPUTS</span></span>

## <span data-ttu-id="e7745-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7745-123">NOTES</span></span>

## <span data-ttu-id="e7745-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7745-124">RELATED LINKS</span></span>

[<span data-ttu-id="e7745-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="e7745-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


