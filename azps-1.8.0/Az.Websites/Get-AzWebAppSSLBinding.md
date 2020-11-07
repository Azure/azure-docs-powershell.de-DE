---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: a50716315796d46185b67099784bc550295231e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658556"
---
# <span data-ttu-id="42a14-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="42a14-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="42a14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42a14-102">SYNOPSIS</span></span>
<span data-ttu-id="42a14-103">Ruft eine Azure Web App-Zertifikat SSL-Bindung ab.</span><span class="sxs-lookup"><span data-stu-id="42a14-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="42a14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a14-104">SYNTAX</span></span>

### <span data-ttu-id="42a14-105">S1</span><span class="sxs-lookup"><span data-stu-id="42a14-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42a14-106">S2</span><span class="sxs-lookup"><span data-stu-id="42a14-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42a14-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42a14-107">DESCRIPTION</span></span>
<span data-ttu-id="42a14-108">Das Cmdlet " **Get-AzWebAppSSLBinding** " Ruft eine SSL-Bindung (Secure Sockets Layer) für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="42a14-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="42a14-109">SSL-Bindungen werden verwendet, um eine Web-App mit einem hochgeladenen Zertifikat zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="42a14-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="42a14-110">Web-Apps können an mehrere Zertifikate gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="42a14-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="42a14-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42a14-111">EXAMPLES</span></span>

### <span data-ttu-id="42a14-112">Beispiel 1: Abrufen von SSL-Bindungen für eine Web-App</span><span class="sxs-lookup"><span data-stu-id="42a14-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="42a14-113">Dieser Befehl ruft die SSL-Bindungen für das Web App ContosoWebApp ab, das der Ressourcengruppe ContosoResourceGroup zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="42a14-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="42a14-114">Beispiel 2: Verwenden eines Objektverweises zum Abrufen von SSL-Bindungen für eine Web-App</span><span class="sxs-lookup"><span data-stu-id="42a14-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="42a14-115">Die Befehle in diesem Beispiel erhalten auch die SSL-Bindungen für das Web App ContosoWebApp; in diesem Fall wird jedoch anstelle des Web App-namens und des Namens der zugeordneten Ressourcengruppe ein Objektverweis verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a14-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="42a14-116">Dieser Objektverweis wird mit dem ersten Befehl im Beispiel erstellt, der mithilfe von **Get-AzWebApp** einen Objektverweis auf die Web-App mit dem Namen ContosoWebApp erstellt.</span><span class="sxs-lookup"><span data-stu-id="42a14-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="42a14-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $webapp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="42a14-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="42a14-118">Diese Variable und das Cmdlet " **Get-AzWebAppSSLBinding** " werden dann vom zweiten Befehl verwendet, um die SSL-Bindungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42a14-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="42a14-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="42a14-119">PARAMETERS</span></span>

### <span data-ttu-id="42a14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a14-120">-DefaultProfile</span></span>
<span data-ttu-id="42a14-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42a14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42a14-122">-Name</span><span class="sxs-lookup"><span data-stu-id="42a14-122">-Name</span></span>
<span data-ttu-id="42a14-123">Gibt den Namen der SSL-Bindung an.</span><span class="sxs-lookup"><span data-stu-id="42a14-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a14-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a14-124">-ResourceGroupName</span></span>
<span data-ttu-id="42a14-125">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="42a14-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="42a14-126">Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="42a14-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a14-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="42a14-127">-Slot</span></span>
<span data-ttu-id="42a14-128">Gibt einen Web App-Bereitstellungs Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="42a14-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="42a14-129">Verwenden Sie das Get-AzWebAppSlot-Cmdlet, um einen Bereitstellungs Steckplatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42a14-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a14-130">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="42a14-130">-WebApp</span></span>
<span data-ttu-id="42a14-131">Gibt eine Web-App an.</span><span class="sxs-lookup"><span data-stu-id="42a14-131">Specifies a Web App.</span></span>
<span data-ttu-id="42a14-132">Verwenden Sie das Get-AzWebApp-Cmdlet, um eine Web-App abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42a14-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42a14-133">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="42a14-133">-WebAppName</span></span>
<span data-ttu-id="42a14-134">Gibt den Namen der Web-App an, von der dieses Cmdlet SSL-Bindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="42a14-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="42a14-135">Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="42a14-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a14-136">CommonParameters</span></span>
<span data-ttu-id="42a14-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a14-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a14-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a14-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42a14-139">INPUTS</span></span>

### <span data-ttu-id="42a14-140">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="42a14-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="42a14-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42a14-141">OUTPUTS</span></span>

### <span data-ttu-id="42a14-142">Microsoft. Azure. Management. Websites. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="42a14-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="42a14-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="42a14-143">NOTES</span></span>

## <span data-ttu-id="42a14-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42a14-144">RELATED LINKS</span></span>

[<span data-ttu-id="42a14-145">Neu – AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="42a14-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="42a14-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="42a14-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="42a14-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a14-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


