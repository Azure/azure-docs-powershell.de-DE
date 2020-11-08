---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005889"
---
# <span data-ttu-id="a51da-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="a51da-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="a51da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a51da-102">SYNOPSIS</span></span>
<span data-ttu-id="a51da-103">Ermöglicht den Remotedesktopzugriff auf einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="a51da-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="a51da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a51da-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a51da-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a51da-105">DESCRIPTION</span></span>
<span data-ttu-id="a51da-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a51da-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a51da-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a51da-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a51da-108">Das Cmdlet **enable-AzureServiceProjectRemoteDesktop** ermöglicht den Remote Desktop Zugriff auf einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="a51da-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="a51da-109">Sie müssen den Dienst mithilfe des Cmdlets **Publish-AzureServiceProject** veröffentlichen, nachdem Sie den Remote Desktop Zugriff aktiviert haben, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="a51da-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="a51da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a51da-110">EXAMPLES</span></span>

## <span data-ttu-id="a51da-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a51da-111">PARAMETERS</span></span>

### <span data-ttu-id="a51da-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a51da-112">-PassThru</span></span>
<span data-ttu-id="a51da-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a51da-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a51da-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a51da-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a51da-115">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="a51da-115">-Password</span></span>
<span data-ttu-id="a51da-116">Gibt das Kennwort an.</span><span class="sxs-lookup"><span data-stu-id="a51da-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51da-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a51da-117">-Profile</span></span>
<span data-ttu-id="a51da-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a51da-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a51da-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a51da-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a51da-120">-Username</span><span class="sxs-lookup"><span data-stu-id="a51da-120">-Username</span></span>
<span data-ttu-id="a51da-121">Gibt den Benutzernamen an, der beim Herstellen einer Verbindung mit der Rolleninstanz in Azure über das Remote Desktop Protokoll (RDP) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a51da-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51da-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51da-122">CommonParameters</span></span>
<span data-ttu-id="a51da-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51da-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51da-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a51da-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51da-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a51da-125">INPUTS</span></span>

## <span data-ttu-id="a51da-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a51da-126">OUTPUTS</span></span>

## <span data-ttu-id="a51da-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a51da-127">NOTES</span></span>

## <span data-ttu-id="a51da-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a51da-128">RELATED LINKS</span></span>

[<span data-ttu-id="a51da-129">Deaktivieren-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="a51da-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="a51da-130">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a51da-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


